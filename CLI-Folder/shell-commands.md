
Introducing the Shell	
A shell is a program whose primary purpose is to read commands and run other programs.

The shell’s main advantages are its high action-to-keystroke ratio, its support for automating repetitive tasks, and its capacity to access networked machines.

The shell’s main disadvantages are its primarily textual nature and how cryptic its commands and operation can be.

Navigating Files and Directories	
The file system is responsible for managing information on the disk.

Information is stored in files, which are stored in directories (folders).

Directories can also store other directories, which forms a directory tree.

cd path changes the current working directory.

ls path prints a listing of a specific file or directory; ls on its own lists the current working directory.

pwd prints the user’s current working directory.

/ on its own is the root directory of the whole file system.

A relative path specifies a location starting from the current location.

An absolute path specifies a location from the root of the file system.

Directory names in a path are separated with / on Unix, but \ on Windows.

.. means ‘the directory above the current one’; . on its own means ‘the current directory’.

Working With Files and Directories	
cp old new copies a file.

mkdir path creates a new directory.

mv old new moves (renames) a file or directory.

rm path removes (deletes) a file.

* matches zero or more characters in a filename, so *.txt matches all files ending in .txt.

? matches any single character in a filename, so ?.txt matches a.txt but not any.txt.

Use of the Control key may be described in many ways, including Ctrl-X, Control-X, and ^X.

The shell does not have a trash bin: once something is deleted, it’s really gone.

Most files’ names are something.extension. The extension isn’t required, and doesn’t guarantee anything, but is normally used to indicate the type of data in the file.

Depending on the type of work you do, you may need a more powerful text editor than Nano.

Pipes and Filters	
cat displays the contents of its inputs.

head displays the first 10 lines of its input.

tail displays the last 10 lines of its input.

sort sorts its inputs.

wc counts lines, words, and characters in its inputs.

command > file redirects a command’s output to a file (overwriting any existing content).

command >> file appends a command’s output to a file.

first | second is a pipeline: the output of the first command is used as the input to the second.

The best way to use the shell is to use pipes to combine simple single-purpose programs (filters).

Loops	
A for loop repeats commands once for every thing in a list.

Every for loop needs a variable to refer to the thing it is currently operating on.

Use $name to expand a variable (i.e., get its value). ${name} can also be used.

Do not use spaces, quotes, or wildcard characters such as ‘*’ or ‘?’ in filenames, as it complicates variable expansion.

Give files consistent names that are easy to match with wildcard patterns to make it easy to select them for looping.

Use the up-arrow key to scroll up through previous commands to edit and repeat them.

Use Ctrl+R to search through the previously entered commands.

Use history to display recent commands, and !number to repeat a command by number.

Shell Scripts	
Save commands in files (usually called shell scripts) for re-use.

bash filename runs the commands saved in a file.

$@ refers to all of a shell script’s command-line arguments.

$1, $2, etc., refer to the first command-line argument, the second command-line argument, etc.

Place variables in quotes if the values might have spaces in them.

Letting users decide what files to process is more flexible and more consistent with built-in Unix commands.

Finding Things	
find finds files with specific properties that match patterns.

grep selects lines in files that match patterns.

--help is an option supported by many bash commands, and programs that can be run from within Bash, to display more information on how to use these commands or programs.

man command displays the manual page for a given command.

$(command) inserts a command’s output in place.

Source: https://swcarpentry.github.io/shell-novice/reference/
