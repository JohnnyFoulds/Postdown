# Debug

To test the packages without installing it, use the following:

```bash
python -m postdown.cmdline demo/storage_document.json demo/storage_document.md
```

_If you are using Windows Subsystem for Windows, you can navigate to `\\wsl$` to access the file system outside the shell._

To deploy from github:

```bash
pip install -e git+https://github.com/JohnnyFoulds/Postdown#egg=postdown
```

## Web References

- [How to fix “Attempted relative import in non-package” even with __init__.py](https://stackoverflow.com/questions/11536764/how-to-fix-attempted-relative-import-in-non-package-even-with-init-py)
- [Pull Request, ignore some file changes](https://stackoverflow.com/questions/28703140/pull-request-ignore-some-file-changes)