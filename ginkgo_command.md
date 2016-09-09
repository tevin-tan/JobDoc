
# ginkgo  #
- A Golang BDD Testing Framwork

- [获取方式](#获取方式#)

* [1.基本框架设计](#1)

	* [1.1图片](#获取)
	
	* [1.2换行](#1.2)
	
	* [1.3强调](#1.3)


<h2 id="获取">1. 获取方式:</h2>
	$ go get github.com/onsi/ginkgo/ginkgo
	$ go get github.com/onsi/gomega
	       
2. 生成测试套件 
--------------------
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



## 3.添加测试用例 ##
 
	$ ginkgo generate book

This will generate a file named **book_test.go** containing:
	
	内容：
	package books_test

	import (
		. "/path/to/books"
		. "github.com/onsi/ginkgo"
		. "github.com/onsi/gomega"
	)

	var _ = Describe("Book", func() {

	})



4. 执行测试
- 
1. 	ginkgo / go test
1. 	ginkgo -v 
1. 	go test -ginkgo.v
1. 	ginkgo -v --progress 

> 执行过程记录

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


构建你的规格： Structuring Your Specs