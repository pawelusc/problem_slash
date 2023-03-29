names in ctnumbers that include '/' are causing problems.

To reproduce run
```
theodore analyze_tden
theodore plot_omfrag
```
The second command should printout a python error ending with 
```
...
fp = builtins.open(filename, "w+b")
FileNotFoundError: [Errno 2] No such file or directory: 'pcolor_uhfref/1/1.png'
```

The updated file_parser form [commit](https://github.com/felixplasser/theodore-qc/commit/ca57ce39a485d57768024e14059e0529fb3d806c) fixes this problem.
