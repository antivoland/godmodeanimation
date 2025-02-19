# https://opensource.com/article/18/8/what-how-makefile
.PHONY: clean run

clean:
	rm -rf venv

venv:
	python -m venv venv
	. venv/bin/activate; pip install --upgrade pip; pip install --upgrade -r requirements.txt

# todo: parameterize
run: venv
	. venv/bin/activate; ./train_t2v_run_jump.sh
