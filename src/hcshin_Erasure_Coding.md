<p><a href="#">데이터 스크러빙</a> 구성에 대한 자세한 내용은 링크를 참조하세요.</p>

<div style="background-color:#d9edf7; padding:10px;"><strong>ERASURE CODING</strong></div>

삭제 코딩 풀은 각 오브젝트를 <code>K+M</code>개의 청크로 저장합니다. 이는 <code>K</code>개의 데이터 청크와 <code>M</code>개의 코딩 청크로 나뉩니다. 풀은 <code>K+M</code> 크기로 설정되어, acting set에 있는 각각의 OSD에 하나의 청크가 저장되도록 구성됩니다. 각 청크의 순위(rank)는 오브젝트의 속성으로 저장됩니다.

예를 들어, 삭제 코딩 풀은 다섯 개의 OSD를 사용하도록 (<code>K+M = 5</code>) 구성할 수 있으며, 그 중 두 개 (<code>M = 2</code>)의 손실을 견딜 수 있습니다. 데이터는 <code>K+1</code>개의 샤드가 복구되기 전까지 사용할 수 없습니다.
