# 성능

아래 성능 수치는 문자열과 숫자가 50/50으로 혼합된 크기 `N` 행 x `50` 열의 워크시트에 대한 실행 시간 및 메모리 사용량을 보여 준다. 수치는 임의의 미드 레인지, 기계에서 가져온 (OS: macOS Mojave version 10.14.4, CPU: 3.4 GHz Intel Core i5, RAM: 16 GB 2400 MHz DDR4, HDD: 1 TB, Go Version: `go1.12.4 darwin/amd64`, Commit: [`0660f30`](https://github.com/360EntSecGroup-Skylar/excelize/tree/0660f30cddc06de7883d40eb4f8e4945c18a0252)). 특정 수치는 기계마다 다르지만 추세는 동일해야 합니다.

<table>
    <tr>
        <th>형식</th>
        <th>행</th>
        <th>열</th>
        <th>시간 (s)</th>
        <th>메모리 (MB)</th>
    </tr>
    <tr>
        <td rowspan="10">Set Cell Value</td>
        <td>200</td>
        <td>50</td>
        <td>0.03</td>
        <td>4</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>0.07</td>
        <td>5</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>0.12</td>
        <td>9</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>0.25</td>
        <td>15</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>0.49</td>
        <td>53</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>1.01</td>
        <td>101</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>2.06</td>
        <td>137</td>
    </tr>
    <tr>
        <td>25600</td>
        <td>50</td>
        <td>4.10</td>
        <td>237</td>
    </tr>
    <tr>
        <td>52100</td>
        <td>50</td>
        <td>8.44</td>
        <td>437</td>
    </tr>
    <tr>
        <td>102400</td>
        <td>50</td>
        <td>16.78</td>
        <td>1643</td>
    </tr>
    <tr>
        <td rowspan="1">Add Chart</td>
        <td>200</td>
        <td>50</td>
        <td>10.6</td>
        <td>171</td>
    </tr>
    <tr>
        <td rowspan="7">Set HyperLink</td>
        <td>200</td>
        <td>50</td>
        <td>0.08</td>
        <td>9</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>0.15</td>
        <td>16</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>0.31</td>
        <td>41</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>0.59</td>
        <td>63</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>1.16</td>
        <td>132</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>2.40</td>
        <td>253</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>4.94</td>
        <td>748</td>
    </tr>
    <tr>
        <td rowspan="7">Insert Picture</td>
        <td>200</td>
        <td>50</td>
        <td>0.86</td>
        <td>40</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>1.83</td>
        <td>79</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>4.11</td>
        <td>158</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>10.07</td>
        <td>316</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>28.17</td>
        <td>632</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>87.90</td>
        <td>1263</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>299.32</td>
        <td>2535</td>
    </tr>
</table>

## 유사한 라이브러리의 성능 비교

다음 그래프는 Go, Python, Java, PHP 와 NodeJS 를 포함한 개인용 컴퓨터의 주요 오픈 소스 Excel libs 에 의한 세대 `12800*50` 일반 텍스트 매트릭스의 성능 비교를 보여줍니다 (OS: macOS Mojave version 10.14.4, CPU: 3.4 GHz Intel Core i5, RAM: 16 GB 2400 MHz DDR4, HDD: 1 TB).

<p align="center"><img width="721" src="https://xuri.me/wp-content/uploads/2016/08/excelize-golang-library-for-reading-and-writing-xlsx-files-3.png" alt="Excel 유사한 라이브러리의 성능 비교"></p>