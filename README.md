<!DOCTYPE html>
<html>
<head>
	<title># Repositori Bahan Ajar Prodi Stratum I Teologi-STT Kalimantan Pontianak</title>
</head>
<body>
	<h1># Repositori Bahan Ajar Prodi Stratum I Teologi-STT Kalimantan Pontianak</h1>
	<p>Check out my latest projects on GitHub:</p>
	<ul>
		<li><a href="https://github.com/username/penelitian">Penelitian</a></li>
		<li><a href="https://github.com/username/Bahan_Ajar_Teologi">Bahan Ajar Teologi</a></li>
		<li><a href="https://github.com/username/Bahan_Ajar_PAK">Bahan Ajar PAK</a></li>
	</ul>
	<?php
		// PHP code to display the last commit message for a repository
		$repo = "username/repo1"; // replace with your own repository name
		$url = "https://api.github.com/repos/$repo/commits";
		$options = array(
			'http' => array(
				'header' => "User-Agent: My PHP Script\r\n"
			)
		);
		$context = stream_context_create($options);
		$response = file_get_contents($url, false, $context);
		$commits = json_decode($response);
		$last_commit = $commits[0]->commit->message;
		echo "<p>Last commit message: $last_commit</p>";
	?>
</body>
</html>
