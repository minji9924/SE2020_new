# Workflow
<br/>

> ## 1. Our team members
Our team has five members. Their information is written below.<br/>
 
| NAME            | Student ID    | Github Link            |
|:----------------|:-------------:| ----------------------:|
| _Yewon Kang_    | 2019054693    | [Yewon Kang](https://github.com/yewonkang00)  |
| _Yejin Kim_     | 2019069034    | [Yejin Kim](https://github.com/yejin00)       |
| _Minji Jun_    | 2019025823    | [Minji Jun](https://github.com/minji9924)    |
| _Yeonju Jeong_  | 2019014739    | [Yeonju Jeong](https://github.com/yeonjujeong)|
| _Subin Han_     | 2019071994    | [Subin Han](https://github.com/hansususu)     | 

<br/>

> ## 2. Our Branch
We have two braches, Branch A and Branch B.

* Branch A
	* Yewon, Minji and Subin will commit and push to Branch A.

* Branch B
	* Yejin and Yeonju will commit and push to Branch B.
<br/>

> ## 3. Workflow Scenario

### 1. Git branch
  <pre><code>
  1. Master 
  &nbsp;&nbsp;&nbsp;&nbsp;제품으로 출시될 수 있는 브랜치
  &nbsp;&nbsp;&nbsp;&nbsp;배포 가능한 상태만을 관리한다.
  2. Develop 
  &nbsp;&nbsp;&nbsp;&nbsp;다음 출시 버전을 개발하는 브랜치
  &nbsp;&nbsp;&nbsp;&nbsp;기능이 추가되고 버그가 수정되어 배포 가능한 안정적인 상태라면 Develop 브랜치를 Master 브랜치에 병합한다.
  3. Feature 
  &nbsp;&nbsp;&nbsp;&nbsp;기능을 개발하는 브랜치
  &nbsp;&nbsp;&nbsp;&nbsp;새로운 기능 개발 및 버그 수정 필요시 Develop 브랜치로부터 분기한다. 
  4. Release 
  &nbsp;&nbsp;&nbsp;&nbsp;이번 출시 버전을 준비하는 브랜치
  &nbsp;&nbsp;&nbsp;&nbsp;배포를 위한 전용 브랜치로 다음 번 배포를 위한 개발 작업과 분리하여 개발을 할 수 있게 해준다.
  5. Hotfix 
  &nbsp;&nbsp;&nbsp;&nbsp; 출시 버전에서 발생한 버그를 수정 하는 브랜치
  </code></pre>

### 2. Git Workflow
  <pre><code>
  1. 깃허브 repository에서 나의 repository에 fork한다.
  
  2. 나의 repository에서 local로 가져오기 위해 clone한다.
  
  3. 내가 fork한 주소를 local로 가져오고, 이를 상대방 repository와 연결한다.
  &nbsp;&nbsp;&nbsp;&nbsp; $ git remote add pair Repo URL for pairs fork
  
  4. 코드를 작성한 후 add, commit을 실행한다.
  &nbsp;&nbsp;&nbsp;&nbsp; $ git add change file
   &nbsp;&nbsp;&nbsp;&nbsp;$ git commit -m "commit message"
   
  5. 나의 github repository (origin)에 push 한다. 
   &nbsp;&nbsp;&nbsp;&nbsp;$ git push origin master
   
  6. 나의 github 저장소에서 Compare & Pull Request 버튼을 선택하여 메시지를 작성하고 PR을 생성한다.

  7. PR을 받은 원본 저장소 관리자는 코드 변경 내역을 확인하고 Merge 여부를 결정한다.

  8. Merge 이후 로컬 코드와 원본 저장소의 코드를 동기화하고, 작업하던 로컬의 branck를삭제한다.
  &nbsp;&nbsp;&nbsp;&nbsp; $ git pull <remote_repo_name>
  &nbsp;&nbsp;&nbsp;&nbsp; $ git branch -d <branch_name>

  9. Merge 이후  변경된 내용은 git pull을 통해 원본 저장소와 동기화를 할 수 있다. 
  &nbsp;&nbsp;&nbsp;&nbsp; $ git pull pair master (or other branch name)

  10. 새로 추가할 기능, 개선해야할 기능, 버그 등 모든 문제 상황은 issue를 등록하여 문제를 해결한다. 
  </code></pre>
  ![KakaoTalk_20201004_181834407](https://user-images.githubusercontent.com/54140431/95012526-40ea4500-0674-11eb-8ac6-5a19fee3bf55.jpg)

## 4. Conflict Prevention

### 1. Competing line change merge conflicts
<pre><code>
1. 팀을 나눈 후, 한 팀이 겹치는 파일을 먼저 고치고 push한다.
After dividing into teams, one team fixes the overlapping files first and push them.

2. 그 다음, 다른 팀은 pull하고 파일을 수정하고 push한다.
The next team should do pull and fix the files and push.

시간 간격을 두어야하며 파일을 수정하기 전에 먼저 pull해야 한다.
Divide the time slot and do pull first before modifying the files.
</pre></code>

### 2. Removed file merge conflicts
<pre><code>
파일을 삭제할 때, 다른 팀원들에게 말한다.
When somebody deletes a file, the person should tell the team members.

파일을 삭제하는 것에 대해 팀원들과 의논한다.
Discuss with team members when deleting files.
</pre></code>

어떤 상황이든 pull과 push를 자주하여 자신의 저장소와 원격 저장소의 상태를 최신으로 유지하는 것이 중요하다.

In any situation, it is important to keep your storage and remote storage up to date by frequent pull and push.


## 5. Workflow

  ![workflow](https://raw.githubusercontent.com/minji9924/SE2020_new/minji1/image/workflow2.png)
