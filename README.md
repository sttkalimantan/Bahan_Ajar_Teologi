# Repositori Bahan Ajar Prodi Stratum I Teologi - STT Kalimantan Pontianak
<!DOCTYPE html>
<html>
<head>
	<title>My GitHub Repository</title>
</head>
<body>
	<h1>My GitHub Repository</h1>
	<p>Check out my latest projects on GitHub:</p>
	<ul>
		<li><a href="https://github.com/username/repo1">Repo 1</a></li>
		<li><a href="https://github.com/username/repo2">Repo 2</a></li>
		<li><a href="https://github.com/username/repo3">Repo 3</a></li>
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
