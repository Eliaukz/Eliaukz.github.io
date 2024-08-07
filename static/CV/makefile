render:
	pandoc --standalone resume.md -t html -c style.css -o resume.html
	awk '/<link rel="stylesheet" href="style.css" \/>/ {print "<style>"; system("cat style.css"); print "</style>"; next} 1' resume.html > temp
	mv temp resume.html
	
	pandoc --standalone --from markdown --to plain -o resume.txt resume.md

html:
	pandoc --standalone resume.md -t html -c style.css -o resume.html

docx:
	pandoc --from markdown --to docx -o resume.docx resume.md
