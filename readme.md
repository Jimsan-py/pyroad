```mermaid
flowchart TD
Data_Structures ==> Data_Management ==> Data_Flows ==> OOP ==> Language_Skeleton ==> Multithreading_&_Multiprocessing ==> Common_Practice ==> Algorithms ==> SQL ==> Net ==> Architecture ==> DevOps

subgraph Data_Structures
direction LR
List(list) -.-> Tuple -.-> Dict -.-> Set -.-> Array -.-> Linked_List -.->Tree -.-> Python_specific_data_structures

subgraph Tuple
direction LR
tuple(tuple)
namedtuple(namedtuple)
end

subgraph Dict
direction LR
dict(dict)
HashProblem("Hash collisions")
defaultdict(defaultdict)
Counter(Counter)
end

subgraph Set
direction LR
set(set)
FrozenSet("frozen set")
end

subgraph Array
direction LR
array(array)
bytes(bytes)
bytearray(bytearray)
end

subgraph Linked_List
direction LR
SinglyLinkedList("Singly linked list")
subgraph Doubly_Linked_List
direction LR
deque(deque)
Queue(Queue)
end
end

subgraph Tree
direction LR
tree(tree)
heap(heap)
B-tree(B-tree)
RedBlackTree("Red–black tree")
AVLTree("AVL tree")
trie(trie)
end

subgraph Python_specific_data_structures
direction LR
enum(enum)
range(range)
dataclass(dataclass)
struct(struct)
string(string)
datetime(datetime)
end
end

subgraph Data_Management
direction LR
slice(slice) -.-> Sorting -.-> Comprehension -.-> bisect(bisect) -.-> Functools -.-> String_Management -.-> Datetime_Management -.->File -.-> Data_Analysis -.-> Neural_Networks
subgraph Sorting
direction LR
sort(sort)
sorted(sorted)
end

subgraph Comprehension
direction LR
listcomprehension(list)
dictcomprehension(dict)
setcomprehension(set)
end

subgraph Functools
direction LR
fmap(map)
ffilter(filter)
freduce(reduce)
fpartial(partial)
fmore(...)
end

subgraph String_Management
direction LR
String_Built-in_Functions("Built-in functions")
regex(regex)
end

subgraph Datetime_Management
direction LR
encode(encode)
decode(decode)
dtmath(math)
end

subgraph File
direction LR
Read_Write("read/write")
Text_Binary("text/binary")
JSON(JSON)
Pickle("Pickle")
Protocol_Buffers("Protocol Buffers")
paths(paths)
end

subgraph Data_Analysis
direction LR
Data_Built-in_Functions("Built-in functions")
NumPy(NumPy)
Pandas(Pandas)
end

subgraph Neural_Networks
direction LR
TensorFlow(TensorFlow)
Keras(Keras)
end

end

subgraph Data_Flows
direction LR

itertools -.-> enumerate -.-> generator -.-> Decorator -.-> context

subgraph itertools
direction LR

subgraph Infinite_Iterators
icount(count)
icycle(cycle)
irepeat(repeat)
end

subgraph Finite_Iterators
pairwise(pairwise)
chain(chain)
fimore(...)
end

subgraph Combinatorics
product(product)
combinations(combinations)
combinations_with_replacement(combinations_with_replacement)
permutations(permutations)
end
end

enumerate(enumerate)
generator(generator)

subgraph Decorator
direction LR
decorator(decorator)
LRUCache("LRU Cache")
param_decorator("Parameterized decorator")
end

context("Context manager")

end

subgraph OOP
direction LR
Class -.-> slots -.-> Object_Copy -.->Inheritance -.-> Metaprogramming

subgraph Class
direction LR
Comparable(Comparable)
Hashable(Hashable)
Sortable(Sortable)
Callable(Callable)
Iterable(Iterable)
Collection(Collection)
Sequence(Sequence)
end

slots(slots)

subgraph Object_Copy
direction LR
shallow("Shallow copy")
deep("Deep copy")
end

subgraph Inheritance
direction LR
objInheritance(Inheritance)
Multiple_Inheritance("Multiple Inheritance")
MRO(MRO)
Inheritance_of_slots("Inheritance of slots")
end

subgraph Metaprogramming
direction LR
Metaclass("Meta Class")
ABCMeta(ABCMeta)
Registry(Registry)
end

end

subgraph Language_Skeleton
subgraph Garbage_Collector
direction LR
reference_counting("Reference counting")
garbage_collector("Garbage collector")
debug_objgraph("GC debug / objgraph")
pypygc("PyPy GC")
end
GIL(GIL)
args_kwargs("*args, **kwargs")
lambda(lambda)
Conditional_Expression("Conditional Expression")
Closure(Closure)
subgraph Exception
direction LR
exception_handling("Exception handling")
built_in_exceptions("Built-in exceptions")
exception_raising("Exception raising")
user_exception("User exceptions")
exception_object("Exception Object")
end
subgraph Introspection
direction LR
variables(variables)
attributes(attributes)
parameters(parameters)
end
Operator(Operator)
end

subgraph Multithreading_&_Multiprocessing
direction LR

Multithreading -.-> asyncio -.-> Multiprocessing -.->Synchronization

subgraph Multithreading
direction LR
Thread(Thread)
Thread_Pool_Executor("Thread pool executor")
Timer
end

subgraph asyncio
direction LR
subgraph High_level_API
create_task(create_task)
gather(gather)
wait_for(wait_for)
hilapi_more("...")
end
subgraph asyncio_Queues
asQueue(Queue)
asPriorityQueue(PriorityQueue)
asLifoQueue(LifoQueue)
end
subgraph asyncio_Streams
StreamReader(StreamReader)
StreamWriter(StreamWriter)
end
subgraph Low_level_API
new_event_loop(new_event_loop)
run_forever(run_forever)
lowlapi_more("...")
end
end

subgraph Multiprocessing
direction LR
Pool(Pool)
Process(Process)
Pipe(Pipe)
Value(Value)
muArray(Array)
Manager(Manager)
Listener(Listener)
end

subgraph Synchronization
direction LR
Lock(Lock)
Event(Event)
Condition(Condition)
Semaphore(Semaphore)
BoundedSemaphore(BoundedSemaphore)
Barrier(Barrier)
end

end

subgraph Common_Practice
direction LR

Logging -.-> Profiling -.-> Random -.-> Input -.-> Print -.-> Cryptography -.-> Testing

Logging(Logging)

subgraph Profiling
direction LR
Stopwatch(Stopwatch)
perf_counter(perf_counter)
timeit
Call_Graph("Call Graph")
end

Random(Random)

subgraph Input
direction LR
input(input)
Command_Line_Arguments("Command Line Arguments")
Argument_Parser("Argument Parser")
end

subgraph Print
direction LR
simple_print(print)
json_print("json print")
Pretty_Print("Pretty Print")
end

subgraph Cryptography
direction LR
MD5(MD5)
AES("AES")
end

subgraph Testing
direction LR
pytest(pytest)
mock(mock)
end

end

subgraph Algorithms
direction LR
FizzBuzz -.-> bigo -.-> Sort -.-> Graphs -.-> Search -.-> Methods
Recursion ==> Recursion

FizzBuzz(FizzBuzz)
bigo("O(n)")

subgraph Sort
direction LR
BubbleSort(BubbleSort)
QuickSort(QuickSort)
MergeSort(MergeSort)
HeapSort(HeapSort)
InsertionSort(InsertionSort)
RadixSort(RadixSort)
end

subgraph Graphs
direction LR
Adjacency_Matrix("Adjacency matrix")
Incidence_Matrix("Incidence matrix")
Adjacency_List("Adjacency list")
Incidence_List("Incidence list")
end

subgraph Search
direction LR
Linear_Search("Linear search")
Binary_Search("Binary search")
DFS(DFS)
BFS(BFS)
Dijkstras(Dijkstras)
Bellman_Ford("Bellman–Ford")
end

subgraph Methods
direction LR
divide_and_conquer("Divide and conquer")
Dynamic_programming("Dynamic programming")
Greedy_algorithm("Greedy algorithm")
Recursion(Recursion)
methmore("...")
end

end

subgraph SQL
direction LR

DB_Basics -.-> SQL_Basics -.-> SQLite -.-> MySQL -.-> PostgreSQL -.-> ORM

subgraph DB_Basics
direction LR
Relational_model("Relational model")
Transaction("Transaction")
Isolation("Isolation")
Nplusone("N+1 problem")
SQL_injection("SQL injection")
NoSQL(NoSQL)
end

subgraph SQL_Basics
direction LR
DDL(DDL)
DML(DML)
DCL(DCL)
end

subgraph SQLite
direction LR
SQLiteConnect(Connect)
SQLiteWrite(Write)
SQLiteRead(Read)
end

subgraph MySQL
direction LR
MySQLConnect(Connect)
MySQLWrite(Write)
MySQLRead(Read)
end

subgraph PostgreSQL
direction LR
PostgreSQL_benefits("PostgreSQL benefits")
PostgreSQLConnect(Connect)
PostgreSQLWrite(Write)
PostgreSQLRead(Read)
end

subgraph ORM
direction LR
peewee(peewee)
SQLAlchemy(SQLAlchemy)
end

end

subgraph Net
direction LR
REST -.-> HTTP -.-> sockets -.-> Frameworks -.-> API

REST(REST)

subgraph HTTP
direction LR
HTTPS(HTTPS)
CSRF-token(CSRF-token)
end

sockets(sockets)

subgraph Frameworks
direction LR
Flask(Flask)
Django(Django)
aiohttp(aiohttp)
end

subgraph API
direction LR
FastAPI(FastAPI)
jwt_tokens("JWT tokens")
end

end

subgraph Architecture
direction LR
WhatIsArch -.-> Principles -.-> Paradigms -.-> Object-oriented -.-> Practices -.-> Microservices -.-> Messaging

WhatIsArch("What is?")
subgraph Principles
direction LR

subgraph SOLID
SRP(SRP)
OCP(OCP)
LSP(LSP)
ISP(ISP)
DIP(DIP)
end

KISS(KISS)
DRY(DRY)
YAGNI(YAGNI)
coupling_vs_cohesion("Coupling vs cohesion")

end

subgraph Paradigms
direction LR
Procedural(Procedural)
Structured(Structured)
parObject-oriented(Object-oriented)
Functional(Functional)
end

subgraph Object-oriented
direction LR
ooInheritance(Inheritance)
Encapsulation(Encapsulation)
Polymorphism(Polymorphism)
Abstraction(Abstraction)
end

subgraph Practices
direction LR
Agile(Agile)
Scrum(Scrum)
Kanban(Kanban)
end

Microservices(Microservices)

subgraph Messaging
direction LR
RabbitMQ(RabbitMQ)
Apache_Kafka("Apache Kafka")
NATS(NATS)
end

end

subgraph DevOps
direction LR
Development_lifecycle -.-> git -.-> Linux -.-> CI_CD -.-> Containers

subgraph Development_lifecycle
direction LR
Git_flow("Git-flow")
trunk_based_development("Trunk-based development")
end
git(git)
Linux(Linux)

subgraph CI_CD
direction LR
Continuous_testing("Continuous testing")
GitHub_Actions("GitHub Actions")
Jenkins(Jenkins)
end

subgraph Containers
direction LR
Docker(Docker)
Kubernetes(Kubernetes)
end

end

classDef dashed stroke-dasharray:5 5
classDef bolded stroke-width:3px,stroke:#f99

class B-tree dashed;
class RedBlackTree dashed;
class AVLTree dashed;
class trie dashed;
class SinglyLinkedList dashed;
class Protocol_Buffers dashed;
class Pandas dashed;
class fmore dashed;
class fimore dashed;
class Metaclass dashed;
class ABCMeta dashed;
class Registry dashed;
class Inheritance_of_slots dashed;
class pypygc dashed;
class Value dashed;
class muArray dashed;
class Manager dashed;
class Listener dashed;
class new_event_loop dashed;
class run_forever dashed;
class lowlapi_more dashed;
class asLifoQueue dashed;
class Timer dashed;
class Low_level_API dashed;
class Metaprogramming dashed;
class Call_Graph dashed;
class Pretty_Print dashed;
class MySQL dashed;
class MySQLConnect dashed;
class MySQLWrite dashed;
class MySQLRead dashed;
class Kubernetes dashed;
class Jenkins dashed;
class NATS dashed;
class aiohttp dashed;
class peewee dashed;
class Neural_Networks dashed;

class NoSQL bolded;
class Functional bolded;
class Microservices bolded;
class RabbitMQ bolded;
class Scrum bolded;
class Apache_Kafka bolded;
class git bolded;
class Linux bolded;
class Docker bolded;
class Cryptography bolded;
class Methods bolded;
class PostgreSQL bolded;
class HTTP bolded;
class SQLAlchemy bolded;
class Flask bolded;
class Django bolded;
class FastAPI bolded;
class ORM bolded;
class TensorFlow bolded;
class Keras bolded;
class regex bolded;
class Testing bolded;
```
