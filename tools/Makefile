quick: gen-zrmdb gen-chai-filter

all: gen-zrmdb gen-chai-filter update-compact-dicts

gen-zrmdb:
	python3 gen_zrmdb.py | sort -k1,1 -s > data/zrmdb.txt

gen-chai-filter:
	python3 gen_chaifen_filter.py > ../opencc/moran_chaifen.txt

dict: update-compact-dicts

update-compact-dicts:
	./update_compact_dicts.sh

dazhu:
	python3 dazhu.py > dazhu-hant.txt
	python3 dazhu.py --dict ../moran_fixed_simp.dict.yaml > dazhu-hans.txt

.PHONY: quick all dict gen-zrmdb gen-chai-filter update-compact-dicts dazhu
