# csv_to_d3_tree
Parses a CSV data structure into a D3 hierarchy

## Usage:

### Building tree with path
```
var data = [
	{id: 1, path:"/a/b/c", size:1, name:"c"},
	{id: 2, path:"/a/d/e", size:3, name:"e"},
	{id: 3, path:"/a/d/f", size:2, name:"f"},
	{id: 4, path:"/a/g", size:5, name:"g"},
	{id: 5, path:"/a/h/i", size:2, name:"i"}
];

var csvToTree = new CSVTOTree("path", "name", size);
var tree = csvToTree.getTreeWithPath(data, "path");
```

### Building tree with hierarchy
```
var data = [
	{id: 1, lev1:"a", lev2:"b", lev3:"c", size:1, name:"c"},
	{id: 2, lev1:"a", lev2:"d", lev3:"e", size:3, name:"e"},
	{id: 3, lev1:"a", lev2:"d", lev3:"f", size:2, name:"f"},
	{id: 4, lev1:"a", lev2:"g", lev3:"", size:5, name:"g"},
	{id: 5, lev1:"a", lev2:"h", lev3:"i", size:1, name:"i"}
];

var csvToTree = new CSVTOTree("path", "name", size);
var tree = csvToTree.getTreeHierarchy(data, ["lev1", "lev2", "lev3"]);
```