

	Configuración de Github



para crear DRONE_GITHUB_CLIENT y DRONE_GITHUB_SECRET se debe añadir una app en github

Settings > Developer settings > New OAuth App

se abre un formulario que pide:

- Application name
- Homepage URL					(dominio al que se pueda acceder para la autenticación [1])
- Application description
- Authorization callback URL	(*mismo dominio que [1], con puerto [2])

Se generará un Client ID y un Client Secret, que debe incluirse en las variables DRONE_GITHUB_CLIENT y DRONE_GITHUB_SECRET

Ej.
		- DRONE_GITHUB=true
		- DRONE_GITHUB_CLIENT=07634239a676acb2751d							//(Client ID)
		- DRONE_GITHUB_SECRET=ef6164caaa5a68b5bc61c49235ce3f9db63b54e3		//(Client Secret)


la variable DRONE_HOST debe tener el valor http://drone-server:puerto (*mismo puerto que [2])


	Configuración de Gitlab



se obtiene el ID y el Secret y debe editarse las variables:

	+     DRONE_GITLAB=true
	+     DRONE_GITLAB_CLIENT=d9afdc6d533f89b98f0d0d59a87842fe4d62dfc64fe91cf32dc1aa72ba5ce3be
	+     DRONE_GITLAB_SECRET=39d697287309cabec5ea4b61fa29ad4f37698df54c6c5274592a3d4f9b941886
	+     DRONE_GITLAB_URL=http://gitlab.com

