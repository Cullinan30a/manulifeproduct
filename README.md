<!DOCTYPE html>
<html lang="zh-HK">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>宏利保險產品列表</title>
	<style>
    	table {
        	width: 100%;
        	border-collapse: collapse;
    	}
    	th, td {
        	padding: 12px;
        	border: 1px solid #ddd;
        	text-align: left;
    	}
    	th {
        	cursor: pointer;
        	background-color: #f4f4f4;
    	}
    	tr:hover {
        	background-color: #f1f1f1;
    	}
    	#searchInput {
        	margin-bottom: 20px;
        	padding: 10px;
        	width: 100%;
        	font-size: 16px;
        	box-sizing: border-box;
    	}
	</style>
</head>
<body>

<h2>宏利保險產品列表</h2>
<input type="text" id="searchInput" onkeyup="searchTable()" placeholder="搜尋產品或類別...">

<table id="productTable">
	<thead>
    	<tr>
        	<th>產品類別</th>
        	<th>產品範例</th>
        	<th>主要功能簡介</th>
        	<th>English Product Name</th>
    	</tr>
	</thead>
	<tbody>
    	<tr>
        	<td>壽險產品</td>
        	<td>宏利尊尚壽險計劃</td>
        	<td>終身壽險保障，靈活理財選擇</td>
        	<td>Manulife Premier Life Insurance Plan</td>
    	</tr>
    	<tr>
        	<td>健康保險</td>
        	<td>宏利盛世醫療保障計劃</td>
        	<td>全面醫療保障，包括住院和手術費用</td>
        	<td>Manulife Supreme Medical Protection Plan</td>
    	</tr>
    	<tr>
        	<td>意外保險</td>
        	<td>宏利全方位意外保障計劃</td>
        	<td>針對意外事故的高額保障，涵蓋醫療及康復費用</td>
        	<td>Manulife Comprehensive Accident Protection Plan</td>
    	</tr>
    	<tr>
        	<td>儲蓄及投資計劃</td>
        	<td>宏利高息儲蓄計劃</td>
        	<td>提供保證回報，兼具靈活理財功能</td>
        	<td>Manulife High Return Savings Plan</td>
    	</tr>
    	<tr>
        	<td>退休計劃</td>
        	<td>宏利退休儲蓄計劃</td>
        	<td>提供長期穩定收益，為退休提供財務保障</td>
        	<td>Manulife Retirement Savings Plan</td>
    	</tr>
    	<tr>
        	<td>強積金計劃</td>
        	<td>宏利MPF計劃</td>
        	<td>香港強制性公積金計劃，針對長期退休儲蓄</td>
        	<td>Manulife MPF Plan</td>
    	</tr>
    	<tr>
        	<td>高端醫療保險</td>
        	<td>宏利私人醫療服務保險計劃</td>
        	<td>提供全球頂級醫療保障，無上限醫療支出</td>
        	<td>Manulife Private Medical Insurance Plan</td>
    	</tr>
    	<tr>
        	<td>重疾保障</td>
        	<td>宏利全面重疾保障計劃</td>
        	<td>覆蓋各類重大疾病，提供長期財務支持</td>
        	<td>Manulife Critical Illness Comprehensive Protection Plan</td>
    	</tr>
	</tbody>
</table>

<script>
// 搜尋功能
function searchTable() {
	var input, filter, table, tr, td, i, j, txtValue, visible;
	input = document.getElementById("searchInput");
	filter = input.value.toLowerCase();
	table = document.getElementById("productTable");
	tr = table.getElementsByTagName("tr");

	for (i = 1; i < tr.length; i++) {
    	visible = false;
    	td = tr[i].getElementsByTagName("td");
    	for (j = 0; j < td.length; j++) {
        	if (td[j]) {
            	txtValue = td[j].textContent || td[j].innerText;
            	if (txtValue.toLowerCase().indexOf(filter) > -1) {
                	visible = true;
                	break;
            	}
        	}
    	}
    	tr[i].style.display = visible ? "" : "none";
	}
}
</script>

</body>
</html>
