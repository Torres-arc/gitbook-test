1. 安装pandoc
https://pandoc.org/installing.html

2. 生成word
mds='' && find . -name "*.md" | sort | while read line; do mds="$mds $line"; done
eval "pandoc -s --reference-doc reference.docx -o ./testcases.docx $mds"

3. 生成html
mds='' && find . -name "*.md" | sort | while read line; do mds="$mds $line"; done
eval "pandoc -s --toc --template=template.html --metadata pagetitle='测试用例' -o ./testcases.html $mds"
