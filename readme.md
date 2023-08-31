

## Description

Provides a real-time Word Count and character count in the status-bar for Sublime Text. See: http://www.sublimetext.com/

Count words and/or characters and Chinese characters on document or in selections. By default, whitespace is not included in the character count.

The minimal word length is 1 and does not count digits.

An estimated reading time is now appended to the end of the word count.

基于[titoBouzout/WordCount](https://github.com/titoBouzout/WordCount) 支持统计中文字符数

## Installation

Zipped file:
1. Locate the Packages directory for Sublime Text.
2. Download the zipped contents of this repository into Packages.
3. Unzip the zipped file. It will create a new directory in Packages.
4. Re-start Sublime Text.

Cloned files:
1. Locate the Packages directory for Sublime Text.
2. In the Packages directory, create a sub-directory called WordCount.
3. Clone the contents of this repository to your new WordCount folder.
4. Re-start Sublime Text.

## Preferences
Located under Sublime Text>Preferences>Package Settings>Settings — User
(You probably need to copy the default settings from the uneditable Sublime Text>Preferences>Package Settings>Settings — **Default**)

 - `enable_live_count` : true

		Allows to control if the live word counter is enabled. Otherwise will be enabled for selections only.

 - `enable_readtime` : false

		Allows you to control if the estimated reading time is enabled.
		Reading time is only displayed when there is a time > 1s.

 - `readtime_wpm` : 200

		Sets the WPM to calculate the Estimated Reading Time for the file.

 - `whitelist_syntaxes` : []

		An array of syntax names that WordCount should run on.
		Example: ["Plain text", "Markdown"]
		If the array is empty, like it is by default, WordCount will run on any syntax.

 - `blacklist_syntaxes` : []

		An array of syntax names that WordCount should not run on.
		Example: ["Plain text", "Markdown"]
		If the array is empty, like it is by default, WordCount will run on any syntax.

 - `char_ignore_whitespace` : true

		Whether to skip whitespace for the character count.

 - `enable_line_word_count` : false

		Display the count of words found on current line.

 - `enable_line_char_count` : false

		Display the count of characters found on current line.

 - `enable_count_lines` : false

		Display the number of lines in file

 - `enable_count_chars` : false

		Display the number of characters in file

 - `enable_count_pages` : true

		Display the number of pages in file

 - `page_count_mode_count_words` : true

		Sets the page count mode to words per page

 - `words_per_page` : 300

		Sets the number of words per page used to calculate number of pages

 - `word_regexp` : ""

		Word Regular expression. Defaults empty, an internal regular expression is used. If the portion of text matches this RegExp then the word is counted.

 - `word_split` : ""

		Split portions of text to test later as words with a Regular expression. Defaults to String.split() with no arguments, means that content will trim() and empty values (all whitespaces) are not used. In case of containing some value different than empty, the return of "re.findall" will be used.

 - `split`: {}

		Remove regex patterns by syntax. Use lowercase for the syntax names.

		Example to ignore all tags, including comments, from HTML:
		
		```
		"strip": {
			"html": [
				"<[^>]*>"
			]
		}
		```
