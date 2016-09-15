
* [ginkgo执行](#1)	
	* [所有哟你](#2)
	* [单元](#3)						
	* [指定执行用例](#4)		
	* [略过用例](#5)
	* [指定非执行用例](#6)
	* [执行过程中不显示颜色](#7)
	* [keepGoing](#8)
	* [ginkgo -p](#9)
	* [并发](#10)



<h2 id="1">执行方式</h2>
<h3 id="2">【显示所有执行过程】</h3>

	ginkgo -v  
<h3 id="3">【单元测试】</h3>
	go test   
<h3 id="4">【指定执行某块部分】</h3>
	ginkgo -v foucus="xxx" .  
<h3 id="5">【指定并跳过某部分用例】</h3>
	ginkgo -v -focus="outer describe"  -skip="A" .
<h3 id="6">【指定非执行用例】</h3>
	ginkgo -v unfocus="should be a pleasant experience" .
<h3 id="7">【执行过程中不显示颜色】</h3>
	ginkgo -v -noColor=true .
<h3 id="8">【当真正的，从早期的测试套件失败，不妨碍以后的测试套件运行】</h3>
	ginkgo -v -keepGoing=true .
<h3 id="9">【ginkgo -p】</h3>
	 ginkgo -p -nodes=1 -v
	 ginkgo -p -nodes=3 -v
<h3 id="10">【并发】</h3>
	ginkgo -nodes=2 -v -stream



