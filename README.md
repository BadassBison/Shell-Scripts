# Bash Scripts

This is a directory to store Bash Scripts. To use this directory effectively, 
make sure to update your PATH with the location of this diretory. If you are 
unsure how to update your PATH, follow the steps below

1. In terminal, `cd` into the directory
2. type `pwd` into the terminal (save this, I'll refer to this as $dirPath)
3. Open your .bashrc file in an editor > `nano ~/.bashrc`
    - If none exists this will create it
4. On the top line add `PATH="$dirPath:$Path"`
5. type `ctrl-x`
6. type `y` to save
7. in terminal, type `source ~/.bashrc`

Once you have this on your PATH, bash will be able to locate the file names and
run them with the name of the file. This is most effective if you leave off the
`.sh` from the file names. Everything at the root level of this directory can 
now be called by simply typing the name of the file into your terminal.