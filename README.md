# 42Cursus_libft
primer ejercicio del curso 42
<p>leaks<p>
  void leaks(void)
{
	system("leaks -q a.out");
}

int main()
{
	char  **sp;
	size_t i = 0;
	char cad[] = "hola separador  de espacio  ";
	sp = ft_split(cad, ' ');
	char *prueba;

	while(i < 4)
	{
		prueba = sp[i];
		printf("PR: %s\n", prueba);
		free(prueba);
		i++;
	}
	free(sp);
	//atexit(leaks);
	//system("leaks -q a.out");
}

<p>testers<p>

https://github.com/alelievr/libft-unit-test escudos
https://github.com/Tripouille/libftTester tripouille
