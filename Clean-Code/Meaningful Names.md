# Meaningful Names
![Image of children neading a name.](http://www.javaskool.com/codeResources/CleanCodeChapters/cleancodePics/meaningfulNames.png)

Names are everywhere in software. We name our variables, functions, arguments, classes and packages. We name our source files and the directories that contain them. We name our jar files and war files and ear files. Because we do so much of it, we’d better do it well.

### Use Intention-Revealing Names
We are serious about it.

```
int d; // elapsed time in days
int elapsedTimeInDays;
```

```
public List<int[]> getThem() {
    List<int[]> list1 = new ArrayList<int[]>();
    for(int[] x : theList)
        if(x[0] == 4)
            list1.add(x);
    return list1;
}

public List<int[]> getFlaggedCells() {
    List<int[]> flaggedCells = new ArrayList<int[]>();
    for(int[] cell : gameBoard)
        if(cell[STATUS_VALUE] == FLAGGED)
            flaggedCells.add(cell);
    return flaggedCells;
}

public List<Cell> getFlaggedCells() {
    List<Cell> flaggedCells = new ArrayList<Cell>();
    for(Cell cell : gameBoard)
        if(cell.isFlagged())
            flaggedCells.add(cell);
    return flaggedCells;
}
```

### Avoid Disambiguation
Do not refer to a grouping of accounts as an `accountList` unless it's actually a List.

Beware of using names which vary in small ways. How long does it take to spot the subtle difference between a `XYZControllerForEfficientHandlingOfStrings` in one module and, somewhere a little more distant, `XYZControllerForEfficientStorageOfStrings`? 


### Make Meaningful Distinctions
```
getActiveAccount();
getActiveAccounts();
getActiveAccountsInfo();
```

### Use Pronounceable Names
If you can't pronounce it you can't discuss it without sounding like an idiout. "Well, over here on the bee cee arr three cee enn tee we have a pee ess zee kyew int, see?"

### Use Searchable Names
The length of a name should correspond to the size of its scope.

### Avoid Encodings

### Hungarian Notation
Not required anymore.

### Member Prefixes
Not required anymore, just adds up to the clutter. You sould be using a programming environment that highlights or colorizes members to make them distinct.

### Interfaces and Implementations
These are sometimes special case for encodings. Avoid using `I` for an interface, encode the implementation instead, i.e. instead of `IShapeFactory` implemented by `ShapeFactory`, use `ShapeFactory` implemented by `ShapeFactoryImpl`.

### Avoid Mental Mapping

### Class Names
Classes and objects sould have noun or noun phrase names like `Customer`, `WikiPage`, `Account` and `AddressParser`. Avoid words like `Manager`, `Processor`, `Data` or `Info` in the name of a class. A class name should not be a verb.

### Method Names
Methods should have verb or verb phrase names like `postPayment`, `deletePage`, or `save`. Accessors, mutators and predicates should be named for their value and prefixed with `get`, `set` and `is` according to the javabean standard.

### Don't Be Cute
If names are too clever, they will be memorable only to people who share the author;s sense of humor, and only as long as these people remember the joke.

### Pick One Word per Concept
It's confusing to have `fetch`, `retrieve` and `get` as equivalent methos of different classes.

What is the essential difference between a `DeviceManager` and a `ProtocolController`?

### Don't Pun
Avoid using the same word for two purposes. Using the same term for two different ideas is essentially a pun.

### Use Solution Domain Names

### Use Problem Domain Names

### Add Meaningful Context

### Don't Add Gratuitous Context


