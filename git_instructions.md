# Repository Handling

## To clone the repository for a local copy on your computer:

1. go to the folder you want to clone it to, click on the directory bar and type cmd and press enter.
2. type the following command
    ```
    git clone https://github.com/sbme-tutorials/task1-robot-arm-graph-bio.git
    ```
___________________________________

## To add an existing project from your local drive to this repository:

1. Initialize the local directory (where the project is) as a Git repository.
    ```
    git init
    ```
2. Add the files in your new local repository.
    ```
    git add --all
    ```
3. Commit the files that you've staged in your local repository.
    ```
    git commit -m "your_comment"
    ```
4. In terminal:
    ```
    git remote add origin https://github.com/sbme-tutorials/task1-robot-arm-graph-bio.git
    ```
5. Sets the new remote:
    ```
    git remote -v
    ```
6. Finally, push the changes in your local repository to GitHub.
    
    ```
    git push origin main
    ```

## Notes

* If you're adding changes to existing files in a repository you already cloned , follow steps 2, 3 and 6.

    > git add *my_changed_filename*