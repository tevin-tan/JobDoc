
![alt text](D:\JobDoc\icon\ginkgo.png "Title")
# ginkgo  #
A Golang BDD Testing Framwork

* [基本框架设计](#1)	
	* [获取方式](#获取)
	* [生成测试套](#生成测试套件)						
	* [添加测试用例](#添加测试用例)		
	* [执行测试](#执行测试)
* [构建你的规格](#2)
	* 
									
<h2 id="获取">1. 获取方式:</h2>
	$ go get github.com/onsi/ginkgo/ginkgo
	$ go get github.com/onsi/gomega
	       
<h2 id="生成测试套件">2. 生成测试套件:</h2>

	ginkgo bootstrap
	简单测试： ginkgo / go test
	
This will generate a file named books_suite_test.go containing:

	package books_test
	
	import (
	. "github.com/onsi/ginkgo"
	. "github.com/onsi/gomega"
	
	"testing"
	)
	
	func TestBooks(t *testing.T) {
	RegisterFailHandler(Fail)
	RunSpecs(t, "Books Suite")
	}


<h2 id="添加测试用例">3. 添加测试用例:</h2>
 
	$ ginkgo generate book

This will generate a file named <font color=Blue size=>**book_test.go**</font>  containing:
	
	内容：
	package books_test

	import (
		. "/path/to/books"
		. "github.com/onsi/ginkgo"
		. "github.com/onsi/gomega"
	)

	var _ = Describe("Book", func() {

	})


<h2 id="执行测试">4. 执行测试:</h2>
- 
1. 	ginkgo / go test
1. 	ginkgo -v 
1. 	go test -ginkgo.v
1. 	ginkgo -v --progress 

> <font color=Blue size=>**执行过程记录**</font>

	$ ginkgo #or go test
	
	=== RUN TestBootstrap
	
	Running Suite: Books Suite
	==========================
	Random Seed: 1378936983
	
	Will run 0 of 0 specs
	
	
	Ran 0 of 0 Specs in 0.000 seconds
	SUCCESS! -- 0 Passed | 0 Failed | 0 Pending | 0 Skipped
	
	--- PASS: TestBootstrap (0.00 seconds)
	PASS
	ok      books   0.019s


<h1 id="2">构建你的规格:</h1>
 Structuring Your Specs

Ginkgo makes it easy to write expressive specs that describe the behavior of your code in an organized manner. You use  <font color=Blue>**Describe**</font> and <font color=Blue>**Context**</font> containers to organize your <font color=Blue>**It**</font> specs and you use  <font color=MediumSpringGreen>**BeforeEach**</font> and <font color=MediumSpringGreen>**AfterEach**</font>  to build up and tear down common set up amongst your tests.

Individual Specs: It

You can add a single spec by placing an It block within a Describe or Context container block:


	var _ = Describe("Book", func() {
    It("can be loaded from JSON", func() {
        book := NewBookFromJSON(`{
            "title":"Les Miserables",
            "author":"Victor Hugo",
            "pages":1488
        }`)

        Expect(book.Title).To(Equal("Les Miserables"))
        Expect(book.Author).To(Equal("Victor Hugo"))
        Expect(book.Pages).To(Equal(1488))
    	})
	})
Its may also be placed at the top-level though this is uncommon.



