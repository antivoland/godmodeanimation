# https://opensource.com/article/18/8/what-how-makefile
.PHONY: clean run

clean:
	rm -rf venv
	#rm -rf decord

venv:
	python -m venv venv
	#. venv/bin/activate; pip install --upgrade pip; pip install --upgrade -r requirements.txt
	#. venv/bin/activate; pip install pip; pip install -r requirements.txt
	. venv/bin/activate; pip install -r requirements.txt
	#. venv/bin/activate; pip install --upgrade pip; pip install --upgrade -r requirements-clean.txt

# todo: parameterize
run: venv
	. venv/bin/activate; ./train_t2v_run_jump.sh

decord:
	 https://github.com/dmlc/decord?tab=readme-ov-file#mac-os
	git clone --recursive https://github.com/dmlc/decord
	cd decord; mkdir build && cd build; cmake .. -DUSE_CUDA=0 -DCMAKE_BUILD_TYPE=Release -DFFMPEG_DIR=/opt/homebrew/opt/ffmpeg@4/; make
	#. venv/bin/activate; cd ./decord/python; python setup.py install --user
		#cd decord/python; python setup.py install --user
