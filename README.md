## Test Case

Test repo for 

https://github.com/evilmartians/lefthook/issues/320

`master` branch contains two static analysis error in `public/index.php` on lines 3 and 5.

`test-feature` branch contains commit which fixed one of the errors, but introduced
a new error on line 7.

Pushing `test-feature` to `master` should report the new error from Line 7 and abort.

### Steps

 - Clone the repo.
    ```
    git clone http://github.com/JoyceBabu/lefthook-test
    ```
 - Switch to new directory
    ```
    cd lefthook-test
    ```
 - Checkout `test-feature` branch
    ```
    git checkout test-feature
    ```
 - Install lefthook
    ```
    npm install
    ```
 - Push `test-feature` branch to `origin/master`
    ```
    git push origin test-feature:master
    ```

