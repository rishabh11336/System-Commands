NPPE OCT 2022
 
Problem 1
------------------
script() { 
mv *.txt level1
}

Problem 2
--------------
script() {
mkdir -p /encryption/two-level/binary/positive-offset/
touch /encryption/two-level/binary/positive-offset/encoding-key
ln /encryption/two-level/binary/positive-offset/encoding-key ek
}

*Not working for private case

Problem 3
---------------
script() {
echo "EOF alpha" >> alpha.txt; cat numbers.txt >> alpha.txt
}

*Only 2 out of 3 private case are working

Problem 4
--------------
script() {
ls -l | grep "d......rwx" | grep -o "\S\+$"
}

Problem 5
---------------
script() {
if [[ $(ls -l $1 | grep -e "^-r--------.*") ]] ; then
    echo "Yes"
fi
}

*Public test case is not passing but private are

Problme 6
-------------
script() { 
ls -d $1
if [[ $? -ne 0 ]]; then
        mkdir $1
fi

cd perf_folder
for file in *perf*.c; do
       mv $file ../$1/program_$file
done
}