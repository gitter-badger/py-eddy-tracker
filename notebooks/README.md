python setup.py install
# rm build/sphinx/ doc/python_module/ doc/gen_modules/ -rf
python setup.py build_sphinx
rsync -vrltp doc/python_module notebooks/.   --include '*/' --include '*.ipynb' --exclude '*' --prune-empty-dirs
