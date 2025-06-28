---
kindle-sync:
  bookId: '52863'
  title: >-
    dokumen.pub_database-internals-a-deep-dive-into-how-distributed-data-systems-work-1492040347-9781492040347
  author: Alex  Petrov
  highlightsCount: 75
---
# dokumen.pub_database-internals-a-deep-dive-into-how-distributed-data-systems-work-1492040347-9781492040347
## Metadata
* Author: Alex  Petrov

## Highlights
Databases are modular systems and consist of multiple parts: a transport layer accepting requests, a query processor determining the most efficient way to run queries, an execution engine carrying out the operations, and a storage engine — location: [179]() ^ref-49714

---
The storage engine (or database engine) is a software component of a database management system responsible for storing, retrieving, and managing data in memory and on disk, designed to capture a persistent, long-term memory of each node [REED78]. While databases can respond to complex queries, storage engines look at the data more granularly and offer a simple data manipulation API, allowing users to create, update, delete, and retrieve records. One way to look at this is that database management systems are applications built on top of storage engines, offering a schema, a query language, indexing, transactions, and many other useful features. — location: [182]() ^ref-26271

---
Storage engines such as BerkeleyDB, LevelDB and its descendant RocksDB, LMDB and its descendant libmdbx, Sophia, HaloDB, and many others were developed independently from the database management systems they’re now embedded into. Using pluggable storage engines has enabled database developers to bootstrap database systems using existing storage engines, and concentrate on the other subsystems. — location: [191]() ^ref-57367

---
construct a test cluster and simulate your workloads. Most databases already have stress tools that can be used to reconstruct specific use cases. If there’s no standard stress tool to generate realistic randomized workloads in the database ecosystem, it might be a red flag. If something prevents you from using default tools, you can try one of the existing general-purpose tools, or implement one from scratch. If the tests show positive results, it may be helpful to familiarize yourself with the database code. Looking at the code, it is often useful to first understand the parts of the database, how to find the code for different components, and then navigate through those. — location: [241]() ^ref-27915

---
The service-level agreement (or SLA) is a commitment by the service provider about the quality of provided services. Among other things, the SLA can include information about latency, throughput, jitter, and the number and frequency of failures. — location: [303]() ^ref-19867

---
two groups do not present a full taxonomy of database management systems and there are many other ways they’re — location: [325]() ^ref-58886

---
some sources group DBMSs into three major categories: Online transaction processing (OLTP) databases These handle a large number of user-facing requests and transactions. Queries are often predefined and short-lived. Online analytical processing (OLAP) databases These handle complex aggregations. OLAP databases are often used for analytics and data warehousing, and are capable of handling complex, long-running ad hoc queries. Hybrid transactional and analytical processing (HTAP) These databases combine properties of both OLTP and OLAP stores. — location: [326]() ^ref-34620

---
themes in these representations. Database management systems use a client/server model, where database system instances (nodes) take the role of servers, — location: [350]() ^ref-50983

---
Database management systems use a client/server model, where database system instances (nodes) take the role of servers, and application instances take the role of clients. — location: [351]() ^ref-59583

---
Client requests arrive through the transport subsystem. Requests come in the form of queries, most often expressed in some query language. The transport subsystem is also responsible for communication with other nodes in the database cluster. — location: [353]() ^ref-42202

---
only after the query is interpreted. The parsed query is passed to the query optimizer, which first eliminates impossible and redundant parts of the query, and then attempts to find the most efficient way to execute it based on internal statistics (index cardinality, approximate intersection size, etc.) and data placement (which nodes in the cluster hold the data and the costs associated with its transfer). The optimizer handles both relational operations required for query resolution, usually presented as a dependency tree, and optimizations, such as index ordering, cardinality estimation, and choosing access methods. — location: [360]() ^ref-7010

---
The query is usually presented in the form of an execution plan (or query plan): a sequence of operations that have to be carried out for its results to be considered complete. Since the same query can be satisfied using different execution plans that can vary in efficiency, the optimizer picks the best available plan. — location: [366]() ^ref-4530

---
The parsed query is passed to the query optimizer, which first eliminates impossible and redundant parts of the query, and then attempts to find the most efficient way to execute it based on internal statistics (index cardinality, approximate intersection size, etc.) and data placement (which nodes in the cluster hold the data and the costs associated with its transfer). The optimizer handles both relational operations required for query resolution, usually presented as a dependency tree, and optimizations, such as index ordering, cardinality estimation, and choosing access methods. — location: [361]() ^ref-48537

---
other nodes) are executed by the storage engine. The storage — location: [374]() ^ref-55316

---
The storage engine has several components with dedicated responsibilities: Transaction manager This manager schedules transactions and ensures they cannot leave the database in a logically inconsistent state. Lock manager This manager locks on the database objects for the running transactions, ensuring that concurrent operations do not violate physical data integrity. Access methods (storage structures) These manage access and organizing data on disk. Access methods include heap files and storage structures such as B-Trees (see “Ubiquitous B-Trees”) or LSM Trees (see “LSM Trees”). Buffer manager This manager caches data pages in memory (see “Buffer Management”). Recovery manager This manager maintains the operation log and restoring the system state in case of a failure (see “Recovery”). Together, transaction and lock managers are responsible for concurrency control — location: [374]() ^ref-10414

---
In-memory database management systems (sometimes called main memory DBMS) store data primarily in memory and use the disk for recovery and logging. Disk-based DBMS hold most of the data on disk and use memory for caching disk contents or as a temporary storage. Both types of systems use the disk to a certain extent, but main memory databases store their contents almost exclusively in RAM. — location: [396]() ^ref-46194

---
Main memory database systems are different from their disk-based counterparts not only in terms of a primary storage medium, but also in which data structures, organization, and optimization techniques they use. Databases using memory as a primary data store do this mainly because of performance, comparatively low access costs, and access granularity. Programming for main memory is also significantly simpler than doing so for the disk. Operating systems abstract memory management and allow us to think in terms of allocating and freeing arbitrarily sized memory chunks. On disk, we have to manage data references, serialization formats, freed memory, and fragmentation manually. — location: [403]() ^ref-52301

---
To avoid replaying complete log contents during startup or after a crash, in-memory stores maintain a backup copy. The backup copy is maintained as a sorted disk-based structure, and modifications to this structure are often asynchronous (decoupled from client requests) and applied in batches to reduce the number of I/O operations. During recovery, database contents can be restored from the backup and logs. — location: [423]() ^ref-58106

---
Log records are usually applied to backup in batches. After the batch of log records is processed, backup holds a database snapshot for a specific point in time, and log contents up to this point can be discarded. This process is called checkpointing. It reduces recovery times by keeping the disk-resident database most up-to-date with log entries without requiring clients to block until the backup is updated. — location: [426]() ^ref-48310

---
For some use cases, it is reasonable to assume that an entire dataset is going to fit in memory. Some datasets are bounded by their real-world representations, such as student records for schools, customer records for corporations, or inventory in an online store. Each record takes up not more than a few Kb, and their number is limited. — location: [441]() ^ref-53261

---
Figure 1-2. Data layout in column- and row-oriented stores — location: [459]() ^ref-61904

---
Because data on a persistent medium such as a disk is typically accessed block-wise (in other words, a minimal unit of disk access is a block), a single block will contain data for all columns. This is great for cases when we’d like to access an entire user record, but makes queries accessing individual fields of multiple user records (for example, queries fetching only the phone numbers) more expensive, since data for the other fields will be paged in as well. — location: [479]() ^ref-23662

---
Column-oriented stores are a good fit for analytical workloads that compute aggregates, such as finding trends, computing average values, etc. Processing complex aggregates can be used in cases when logical records have multiple fields, but some of them (in this case, price quotes) have different — location: [488]() ^ref-17053

---
Storing values for different columns in separate files or file segments allows efficient queries by column, since they can be read in one pass rather than consuming entire rows and discarding data for columns that weren’t queried. Column-oriented stores are a good fit for analytical workloads that compute aggregates, such as finding trends, computing average values, etc. Processing complex aggregates can be used in cases when logical records have multiple fields, but some of them (in this case, price quotes) have different importance and are often consumed together. — location: [486]() ^ref-683

---
To reconstruct data tuples, which might be useful for joins, filtering, and multirow aggregates, we need to preserve some metadata on the column level to identify which data points from other columns it is associated with. If you do this explicitly, each value will have to hold a key, which introduces duplication and increases the amount of stored data. Some column stores use implicit identifiers (virtual IDs) instead and use the position of the value (in other words, its offset) to map it back to the related values — location: [498]() ^ref-2924

---
Column-oriented databases should not be mixed up with wide column stores, such as BigTable or HBase, where data is represented as a multidimensional map, columns are grouped into column families (usually storing data of the same type), and inside each column family, data is stored row-wise. This layout is best for storing data retrieved by a key or a sequence of keys. — location: [526]() ^ref-33903

---
Database systems do use files for storing the data, but instead of relying on filesystem hierarchies of directories and files for locating records, they compose files using implementation-specific formats. — location: [559]() ^ref-7974

---
Database systems store data records, consisting of multiple fields, in tables, where each table is usually represented as a separate file. Each record in the table can be looked up using a search key. To locate a record, database systems use indexes: auxiliary data structures that allow it to efficiently locate data records without scanning an entire table on every access. Indexes are built using a subset of fields identifying the record. A database system usually separates data files and index files: data files store data records, while index files store record metadata and use it to locate records in data files. — location: [565]() ^ref-47410

---
index on a primary (data) file is called the primary — location: [611]() ^ref-1437

---
An index on a primary (data) file is called the primary index. However, in most cases we can also assume that the primary index is built over a primary key or a set of keys identified as primary. All other indexes are called secondary. Secondary indexes can point directly to the data record, or simply store its primary key. — location: [609]() ^ref-61750

---
There are different opinions in the database community on whether data records should be referenced directly (through file offset) or via the primary key index. — location: [645]() ^ref-20346

---
Storage structures have three common variables: they use buffering (or avoid using it), use immutable (or mutable) files, and store values in order (or out of order). — location: [674]() ^ref-4148

---
Buffering This defines whether or not the storage structure chooses to collect a certain amount of data in memory before putting it on disk. — location: [677]() ^ref-59450

---
Mutability (or immutability) This defines whether or not the storage structure reads parts of the file, updates them, and writes the updated results at the same location in the file. Immutable structures are append-only: once written, file contents are not modified. Instead, modifications are appended to the end of the file. — location: [685]() ^ref-11573

---
Ordering This is defined as whether or not the data records are stored in the key order in the pages on disk. In other words, the keys that sort closely are stored in contiguous segments on disk. — location: [694]() ^ref-2883

---
element insertion might lead to the situation where the tree is unbalanced (i.e., one of its branches is longer than the other one). The worst-case scenario is shown in Figure 2-3 (b), where we end up with a pathological tree, which looks more like a linked list, and instead of desired logarithmic complexity, we get linear, as illustrated in Figure 2-3 (a). — location: [766]() ^ref-21755

---
The balanced tree is defined as one that has a height of log2 N, where N is the total number of items in the tree, and the difference in height between the two subtrees is not greater than one1 [KNUTH98]. Without balancing, we lose performance benefits of the binary search tree structure, and allow insertions and deletions order to determine tree shape. In the balanced tree, following the left or right node pointer reduces the search space in half on average, so lookup complexity is logarithmic: O(log2 N). If the tree is not balanced, worst-case complexity goes up to O(N), — location: [775]() ^ref-12048

---
One of the ways to keep the tree balanced is to perform a rotation step after nodes are added or removed. If the insert operation leaves a branch unbalanced (two consecutive nodes in the branch have only one child), we can rotate nodes around the middle one. In the example shown in Figure 2-4, during rotation the middle node (3), known as a rotation pivot, is promoted one level higher, and its parent becomes its right child. — location: [787]() ^ref-56315

---
low fanout (fanout is the maximum allowed number of children per node), — location: [798]() ^ref-45817

---
N). Balanced trees give us an average O(log2 N). At the same time, due to low fanout (fanout is the maximum allowed number of children per node), we have to perform balancing, relocate nodes, and update pointers rather frequently. — location: [797]() ^ref-9555

---
If we wanted to maintain a BST on disk, we’d face several problems. One problem is locality: since elements are added in random order, there’s no guarantee that a newly created node is written close to its parent, which means that node child pointers may span across several disk pages. We can improve the situation to a certain extent by modifying the tree layout and using paged binary trees — location: [801]() ^ref-7492

---
Another problem, closely related to the cost of following child pointers, is tree height. Since binary trees have a fanout of just two, height is a binary logarithm of the number of the elements in the tree, and we have to perform O(log2 N) seeks to locate the searched element and, subsequently, perform the same number of disk transfers. 2-3-Trees and other low-fanout trees have a similar limitation: while they are useful as in-memory data structures, small node size makes them impractical for external storage — location: [805]() ^ref-60195

---
Considering these factors, a version of the tree that would be better suited for disk implementation has to exhibit the following properties: High fanout to improve locality of the neighboring keys. Low height to reduce the number of seeks during traversal. Note Fanout and height are inversely correlated: the higher the fanout, the lower the height. If fanout is high, each node can hold more children, reducing the number of nodes and, subsequently, reducing height. — location: [812]() ^ref-49642

---
On spinning disks, seeks increase costs of random reads because they require disk rotation and mechanical head movements to position the read/write head to the desired location. However, once the expensive part is done, reading or writing contiguous bytes (i.e., sequential operations) is relatively cheap. — location: [835]() ^ref-10600

---
The smallest transfer unit of a spinning drive is a sector, so when some operation is performed, at least an entire sector can be read or written. Sector sizes typically range from 512 bytes to 4 Kb. — location: [839]() ^ref-26582

---
Solid state drives (SSDs) do not have moving parts: there’s no disk that spins, or head that has to be positioned for the read. A typical SSD is built of memory cells, connected into strings (typically 32 to 64 cells per string), strings are combined into arrays, arrays are combined into pages, and pages are combined into blocks — location: [844]() ^ref-11657

---
Pages vary in size between devices, but typically their sizes range from 2 to 16 Kb. Blocks typically contain 64 to 512 pages. Blocks are organized into planes and, finally, planes are placed on a die. SSDs can have one or more dies. Figure 2-5 shows this hierarchy. — location: [853]() ^ref-33291

---
The smallest unit that can be written (programmed) or read is a page. However, we can only make changes to the empty memory cells (i.e., to ones that have been erased before the write). The smallest erase entity is not a page, but a block that holds multiple pages, which is why it is often called an erase block. Pages in an empty block have to be written sequentially. — location: [858]() ^ref-19532

---
Since in both device types (HDDs and SSDs) we are addressing chunks of memory rather than individual bytes (i.e., accessing data block-wise), most operating systems have a block device abstraction [CESATI05]. It hides an internal disk structure and buffers I/O operations internally, so when we’re reading a single word from a block device, the whole block containing it is read. This is a constraint we cannot ignore and should always take into account when working with disk-resident data structures. — location: [868]() ^ref-45953

---
To follow a pointer to the specific location within the block, we have to fetch an entire block. — location: [883]() ^ref-64484

---
On disk, most of the time we manage the data layout manually (unless, for example, we’re using memory mapped files). This is still similar to regular pointer operations, but we have to compute the target pointer addresses and follow the pointers explicitly. Most of the time, on-disk offsets are precomputed (in cases when the pointer is written on disk before the part it points to) or cached in memory until they are flushed on the disk. Creating long dependency chains in on-disk structures greatly increases code and structure complexity, so it is preferred to keep the number of pointers and their spans to a minimum. — location: [886]() ^ref-14730

---
B-Trees combine these ideas: increase node fanout, and reduce tree height, the number of node pointers, and the frequency of balancing operations. — location: [898]() ^ref-5239

---
B-Trees can be thought of as a vast catalog room in the library: you first have to pick the correct cabinet, then the correct shelf in that cabinet, then the correct drawer on the shelf, and then browse through the cards in the drawer to find the one you’re searching for. Similarly, a B-Tree builds a hierarchy that helps to navigate and locate the searched items quickly. — location: [911]() ^ref-36294

---
Figure 2-7. Binary tree, 2-3-Tree, and B-Tree nodes side by side — location: [924]() ^ref-61255

---
Tree Lookup Complexity” for more on this subject). If we had to make a disk seek for each one of these comparisons, it would significantly slow us down, but since B-Tree nodes store dozens or even hundreds — location: [935]() ^ref-5014

---
If we had to make a disk seek for each one of these comparisons, it would significantly slow us down, but since B-Tree nodes store dozens or even hundreds of items, we only have to make one disk seek per level jump. — location: [935]() ^ref-18318

---
Using B-Trees, we can efficiently execute both point and range queries. Point queries, expressed by the equality (=) predicate in most query languages, locate a single item. On the other hand, range queries, expressed by comparison (<, >, ≤, and ≥) predicates, are used to query multiple data items in order. — location: [937]() ^ref-52681

---
Since B-Trees are a page organization technique (i.e., they are used to organize and navigate fixed-size pages), we often use terms node and page interchangeably. The relation between the node capacity and the number of keys it actually holds is called occupancy. — location: [956]() ^ref-5040

---
We’re using the term B-Tree as an umbrella for a family of data structures that share all or most of the mentioned properties. A more precise name for the described data structure is B+-Tree. [KNUTH98] refers to trees with a high fanout as multiway trees. B-Trees allow storing values on any level: in root, internal, and leaf nodes. B+-Trees store values only in leaf nodes. Internal nodes store only separator keys used to guide the search algorithm to the associated value stored on the leaf level. Since values in B+-Trees are stored only on the leaf level, all operations (inserting, updating, removing, and retrieving data records) affect only leaf nodes and propagate to higher levels only during splits and merges. B+-Trees became widespread, and we refer to them as B-Trees, — location: [967]() ^ref-12374

---
Keys stored in B-Tree nodes are called index entries, separator keys, or divider cells. They split the tree into subtrees (also called branches or subranges), holding corresponding key ranges. Keys are stored in sorted order to allow binary search. A subtree is found by locating a key and following a corresponding pointer from the higher to the lower level. The first pointer in the node points to the subtree holding items less than the first key, and the last pointer in the node points to the subtree holding items greater than or equal to the last key. Other pointers are reference subtrees between the two keys: Ki-1 ≤ Ks < Ki, where K is a set of keys, and Ks is a key that belongs to the subtree. Figure 2-10 shows these invariants. Figure 2-10. How separator keys split a tree into subtrees — location: [980]() ^ref-56252

---
Some B-Tree variants also have sibling node pointers, most often on the leaf level, to simplify range scans. These pointers help avoid going back to the parent to find the next sibling. Some implementations have pointers in both directions, forming a double-linked list on the leaf level, which makes the reverse iteration possible. What sets B-Trees apart is that, rather than being built from top to bottom (as binary search trees), they’re constructed the other way around—from bottom to top. The number of leaf nodes grows, which increases the number of internal nodes and tree height. Since B-Trees reserve extra space inside nodes for future insertions and updates, tree storage utilization can get as low as 50%, but is usually considerably higher. Higher occupancy does not influence B-Tree performance negatively. — location: [996]() ^ref-37583

---
If the target node doesn’t have enough room available, we say that the node has overflowed — location: [1057]() ^ref-24501

---
Updates in B-Trees work by locating a target leaf node using a lookup algorithm and associating a new value with an existing key. If the target node doesn’t have enough room available, we say that the node has overflowed — location: [1056]() ^ref-9790

---
Big-endian The order starts from the most-significant byte (MSB), followed by the bytes in decreasing significance order. In other words, MSB has the lowest address. Little-endian The order starts from the least-significant byte (LSB), followed by the bytes in increasing significance order. — location: [1209]() ^ref-38884

---
Records consist of primitives like numbers, strings, booleans, and their combinations. However, when transferring data over the network or storing it on disk, we can only use byte sequences. This means that, in order to send or write the record, we have to serialize it (convert it to an interpretable sequence of bytes) and, before we can use it after receiving or reading, we have to deserialize it (translate the sequence of bytes back to the original record). — location: [1229]() ^ref-12039

---
Strings and other variable-size data types (such as arrays of fixed-size data) can be serialized as a number, representing the length of the array or string, followed by size bytes: the actual data. For strings, this representation is often called UCSD String or Pascal String, named after the popular implementation of the Pascal programming language. We can express it in pseudocode as follows: String ^ref-18717
{
size    uint_16
data    byte[size]
} An alternative to Pascal strings is null-terminated strings, where the reader consumes the string byte-wise until the end-of-string symbol is reached. — location: [1262]()

---
Enums, short for enumerated types, can be represented as integers and are often used in binary formats and communication protocols. Enums are used to represent often-repeated low-cardinality values. For example, we can encode a B-Tree node type using an enum: enum NodeType { ^ref-27634
ROOT,     // 0x00h
INTERNAL, // 0x01h
LEAF      // 0x02h
}; — location: [1281]()

---
Many data stores have a fixed schema, specifying the number, order, and type of fields the table can hold. Having a fixed schema helps to reduce the amount of data stored on disk: instead of repeatedly writing field names, we can use their positional identifiers. If we wanted to design a format for the company directory, storing names, birth dates, tax numbers, and genders for each employee, we could use several approaches. We could store the fixed-size fields (such as birth date and tax number) in the head of the structure, followed by the variable-size ones: Fixed-size fields: ^ref-45320
| (4 bytes) employee_id                |
| (4 bytes) tax_number                 |
| (3 bytes) date                       |
| (1 byte)  gender                     |
| (2 bytes) first_name_length          |
| (2 bytes) last_name_length           |
Variable-size fields:
| (first_name_length bytes) first_name |
| (last_name_length bytes) last_name   | — location: [1318]()

---
Figure 3-3. File organization Many data stores have a fixed schema, specifying the number, order, and type of fields the table can hold. Having a fixed schema helps to reduce the amount of data stored on disk: instead of repeatedly writing field names, we can use their positional identifiers. If we wanted to design a format for the company directory, storing names, birth dates, tax numbers, and genders for each employee, we could use several approaches. We could store the fixed-size fields (such as birth date and tax number) in the head of the structure, followed by the variable-size ones: Fixed-size fields: ^ref-11914
| (4 bytes) employee_id                |
| (4 bytes) tax_number                 |
| (3 bytes) date                       |
| (1 byte)  gender                     |
| (2 bytes) first_name_length          |
| (2 bytes) last_name_length           |
Variable-size fields:
| (first_name_length bytes) first_name |
| (last_name_length bytes) last_name   | — location: [1317]()

---
Database systems store data records in data and index files. These files are partitioned into fixed-size units called pages, which often have a size of multiple filesystem blocks. Page sizes usually range from 4 to 16 Kb. — location: [1338]() ^ref-39061

---
in B-Trees, we distinguish between the leaf nodes that hold keys and data records pairs, and nonleaf nodes that hold keys and pointers to other nodes. Each B-Tree node occupies one page or multiple pages linked together, so in the context of B-Trees the terms node and page (and even block) are often used interchangeably. — location: [1344]() ^ref-31930

---
Store variable-size records with a minimal overhead. Reclaim space occupied by the removed records. Reference records in the page without regard to their exact locations. To efficiently store variable-size records such as strings, binary large objects (BLOBs), etc., we can use an organization technique called slotted page — location: [1372]() ^ref-19320

---
We organize the page into a collection of slots or cells and split out pointers and cells in two independent memory regions residing on different sides of the page. This means that we only need to reorganize pointers addressing the cells to preserve the order, and deleting a record can be done either by nullifying its pointer or removing it. — location: [1380]() ^ref-19377

---
To summarize, node splits are done in four steps: Allocate a new node. Copy half the elements from the splitting node to the new one. Place the new element into the corresponding node. At the parent of the split node, add a separator key and a pointer to the new node. — location: [1094]() ^ref-16303

---
To summarize, node merges are done in three steps, assuming the element is already removed: Copy all elements from the right node to the left one. Remove the right node pointer from the parent (or demote it in the case of a nonleaf merge). Remove the right node. — location: [1124]() ^ref-10924

---
