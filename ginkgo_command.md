
# ginkgo  #

----------


A Golang BDD Testing Framework



> Getting Ginkgo

	Just go get it:
	$ go get github.com/onsi/ginkgo/ginkgo
	$ go get github.com/onsi/gomega





-  1. 获取方式:
-  
	$ go get github.com/onsi/ginkgo/ginkgo
	$ go get github.com/onsi/gomega
	       



- 2. 生成测试套件
- 
	ginkgo bootstrap
	简单测试： ginkgo / go test




- 3. 添加测试用例
- 
-**ginkgo generate book**

	
	内容：
	package books_test

	import (
		. "/path/to/books"
		. "github.com/onsi/ginkgo"
		. "github.com/onsi/gomega"
	)

	var _ = Describe("Book", func() {

	})



- 4. 执行测试
- 
	ginkgo / go test
	ginkgo -v 
	go test -ginkgo.v
	ginkgo -v --progress 


