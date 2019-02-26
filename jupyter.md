#### kernel
- list kernel
  ```
  jupyter kernelspec list
  jupyter kernelspec uninstall unwanted-kernel
  ```

- create kernel under virtual env 
  
  **Make sure python used to create kernel is under virtual env.**
  ```
  source activate myenv
  python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
  ```
- remove kernel
  ```
  jupyter kernelspec uninstall unwanted-kernel
  ```
  
