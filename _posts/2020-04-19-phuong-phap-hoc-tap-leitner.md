---
keywords: fastai
description: drafting
title: Giới thiệu phương pháp học Leitner 
toc: true 
badges: true
comments: true
categories: [tutorial]
image: images/leitner_box.jpg
hide: true
nb_path: _notebooks/phuong-phap-hoc-tap-leitner.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/phuong-phap-hoc-tap-leitner.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Gi&#7899;i-thi&#7879;u">Gi&#7899;i thi&#7879;u<a class="anchor-link" href="#Gi&#7899;i-thi&#7879;u"> </a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Những thứ không hiệu quả cho việc học như: bài giảng, nhồi nhét và đọc lại.</p>
<p>Phương pháp này dựa trên việc học tập một kiến thức mới lặp đi lặp lại, chúng ta kiểm tra trí nhớ của mình về một kiến thức nào đó lặp đi lặp lại và trong những khoảng thời gian khác nhau. Phương pháp này không phải là một study trick hay life hack mà là một cách để điều khiển bộ não của mình, giúp não bộ nhớ lâu hơn.
Phương pháp này được phát minh bở nhà tâm lý học người Đức Hermann Ebbinghaus. Ông đã tiến hành một thí nghiệm, theo dõi khả năng nhớ hàng nghìn từ vựng vô nghĩa của mình và ghi chép việc quên của mình. Ông khám phá ra rằng ông đã quên hầu hết mọi thứ đã học trong vòng 24h đầu tiên và những thứ còn xót lại tiếp tục bị quên dần những ngày sau đó. Tuy nhiên, nhìn chung tốc độ quên những thứ đã học giảm dần khi chúng ta được chủ động xem lại kiến thức đó (không phải bị động) - mặc dù khi cyahúng ta dừng thực hành, bộ nhớ tiếp tục giảm. Do vậy, để học bất cứ thứ gì, bạn cần phải xem lại nó ngay lúc bộ não bắt đầu quên và thời gian giữa các lần review phải tăng dần.</p>
<p><a href="images.forgetting_curve.png">forgeting_curve</a></p>
<p>Điều thú vị trong cách học này là bạn không phải học 1 thứ lặp đi lặp lại mà bạn chỉ học thứ mới hoặc thứ bạn cứ quên quài.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="H&#7897;p-Leitner">H&#7897;p Leitner<a class="anchor-link" href="#H&#7897;p-Leitner"> </a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Đầu tiên, chúng ta chia hộp thành 7 cấp độ, bạn có thể có nhiều hoặc ít hơn nếu thích.
Một card mới sẽ được bỏ vào hộp thứ 1, khuyến khich bắt đầu với 5 card mơi mỗi ngày. 
Khi bạn review một card, nếu bạn nhớ đúng kiến thức trong đó, chuyển card đó up một level. Nếu card của bạn ở level cuối cùng, chúc mừng bạn, bây giờ bạn có thể vứt chiệc card đó đi, kiến thức bên trong chiếc card đó sẽ theo bạn suốt đời.
Tuy nhiên nếu bạn quên một card nào đó, bạn phải chuyển nó về hộp ban đầu, hộp đầu tiên.
Thời gian review hộp leitner:</p>
<ul>
<li>level 1: hằng ngày</li>
<li>level 2: 2 ngày một lần</li>
<li>level 3: 4 ngày một lần
... cứ như vậy, mỗi lần lên một bậc thì gấp đôi thời gian review
<a href="schedule"></a>
Mỗi lần review, chúng ta sẽ review level từ trên xuống, như vậy level 1 sẽ được review cuối cùng. Như vậy chúng ta sẽ biết được những card mình bị quên và những card mới bỏ vào.
Hằng ngày, cố gắng không để sót lại bất kì card nào ở level 1, học đi học lại đến khi nào mình nhớ nó và move nó lên level 2.</li>
</ul>
<p>review first =&gt; add new card later</p>
<p>mỗi ngày chúng ta cố dành khoảng 20-30 phút để học thay vì xem tivi - bạn có thể nhớ mọi thứ trên đời. Tuy nhiên để xây dựng được thới quen mới khá khó, nếu bạn khởi đầu lớn, có thể bạn sẽ kết thúc nó ngay ngày hôm sau. Nếu bạn khởi đầu nhỏ và lấy cảm hứng dần dần, bạn có thể học nhiều hơn mỗi ngày, vì vậy mà mình khuyến khích học 5 card mỗi ngày.</p>
<p>Sau khi chúng ta đã quen với cách học này, chúng ta có thể có 10,15,20,25,30 card/ngày.
Nếu bạn học 30 card mỗi ngày, một năm bạn sẽ học được 10.000+ điều mới</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Nh&#7919;ng-vi&#7879;c-c&#243;-th&#7875;-d&#7851;n-t&#7899;i-h&#7885;c-sai">Nh&#7919;ng vi&#7879;c c&#243; th&#7875; d&#7851;n t&#7899;i h&#7885;c sai<a class="anchor-link" href="#Nh&#7919;ng-vi&#7879;c-c&#243;-th&#7875;-d&#7851;n-t&#7899;i-h&#7885;c-sai"> </a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>Việc học sẽ fail nếu những card của bạn cồng kềnh, không liên quan tới nhau và không có nghĩa. Mặc khác nếu những card của bạn là những mảng nhỏ, kết nôi vơi nhau thì sẽ tốt hơn. Đó cũng là cách nao bộ hoạt động, lots of small and connected things. Vấn đề không phải ở chỗ collection mà ở chỗ connection.</li>
</ul>
<p>=&gt; card của bạn phải nhỏ, kết nối, có ý nghĩa.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>Nhỏ: quá nhiều thông tin trên một card =&gt; hãy cắt nhỏ nó ra thành nhiều card, smaller and connected pieces. =&gt; rule of thumb: mỗi card chỉ nếu có một và chỉ một idea. </li>
<li>connected: nếu bạn vẽ hình, ghi hoàn cảnh hoặc thông tin cá nhân lên card, sẽ gợi nhớ tốt hơn có card.</li>
<li><p>ý nghĩa: hãy chọn một topic nào đó mà bạn đang theo đuổi, học piano, đọc truyện, chơi game và bắt đầu dùng leitner box để học mọi thứ về bộ môn đó. Mình tin rằng cách tốt nhất để giữ motivation cho việc học là mình đọc học thứ gì đó mình quan tâm</p>
</li>
<li><p>không quan trọng bạn học buổi sáng hay chiều, quan trọng là hằng ngày đều phải học (đôi khi có thể skip 1 ngày)</p>
</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>you cheat: correct answer, time, </li>
<li>you dont shuffle</li>
<li>you dont cart your victories</li>
<li>you dont educate yourself</li>
<li>your flashcard are wrong</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">www</span><span class="o">.</span><span class="n">youtube</span><span class="o">.</span><span class="n">com</span><span class="o">/</span><span class="n">watch</span><span class="err">?</span><span class="n">v</span><span class="o">=</span><span class="n">HN0OUnLxFeU</span><span class="o">&amp;</span><span class="nb">list</span><span class="o">=</span><span class="n">PLdddsM1tHEe</span><span class="o">-</span><span class="n">I7QpcFmoNsmwP3dWH_3s_</span>
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">www</span><span class="o">.</span><span class="n">youtube</span><span class="o">.</span><span class="n">com</span><span class="o">/</span><span class="n">watch</span><span class="err">?</span><span class="n">v</span><span class="o">=</span><span class="n">hs5qmTKBSU0</span><span class="o">&amp;</span><span class="nb">list</span><span class="o">=</span><span class="n">PLdddsM1tHEe</span><span class="o">-</span><span class="n">I7QpcFmoNsmwP3dWH_3s_</span><span class="o">&amp;</span><span class="n">index</span><span class="o">=</span><span class="mi">3</span>
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">www</span><span class="o">.</span><span class="n">youtube</span><span class="o">.</span><span class="n">com</span><span class="o">/</span><span class="n">watch</span><span class="err">?</span><span class="n">v</span><span class="o">=</span><span class="n">ad1nHS</span><span class="o">-</span><span class="mi">3</span><span class="n">stg</span>
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">ncase</span><span class="o">.</span><span class="n">me</span><span class="o">/</span><span class="n">remember</span><span class="o">/</span>
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">en</span><span class="o">.</span><span class="n">wikipedia</span><span class="o">.</span><span class="n">org</span><span class="o">/</span><span class="n">wiki</span><span class="o">/</span><span class="n">Leitner_system</span>
    
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">www</span><span class="o">.</span><span class="n">ankiapp</span><span class="o">.</span><span class="n">com</span><span class="o">/</span>
<span class="n">https</span><span class="p">:</span><span class="o">//</span><span class="n">tinycards</span><span class="o">.</span><span class="n">duolingo</span><span class="o">.</span><span class="n">com</span><span class="o">/</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 
