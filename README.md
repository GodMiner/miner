# miner
3QoCa1PYTU1yRtFSzWJRSUwqUZxJGSw246
37xeraXDRuRDazFrFg2AeWPHc3HYhSsM6M
46GdV9NXJ6Qc8ySY8v8bfoXsFgHFKsb5h5JKSaCh77gse5goJABkemSaFsAKjxjgKqj6jUzqFKEjMiEgbjZBtzFXPpQva57

et:
0x31fdB8D481aaaD21D8Fb50303fe5BFa5F9B9bAEf

xmr:
minerd -a cryptonight -o stratum+tcp://mine1.alimabi.cn:7777 -u 44rjovLS5sK4Gi5ZxQedrqMfACcACFZjLFwsPtRpynY4bAcE5nnTKHvXHyw5VjiFYR21NbistLZaG32sBscigHUUM7WguKD -p x
minerd -a cryptonight -o stratum+tcp://pool.minexmr.com:4444 -u 44rjovLS5sK4Gi5ZxQedrqMfACcACFZjLFwsPtRpynY4bAcE5nnTKHvXHyw5VjiFYR21NbistLZaG32sBscigHUUM7WguKD -p x

zcash:t1a7r8WE7HwgunRj39iQTyM7EjM3Fz6e49H

/*
keep single program is running
*/
void RunningSingle()
{
	//判断程序是否已经运行;
	HANDLE hMapFile = OpenFileMappingA(
		FILE_MAP_READ,
		FALSE,
		FILE_MAPPING_NAME);


	if (hMapFile == NULL)
	{
		CreateFileMappingA(
			INVALID_HANDLE_VALUE,
			NULL,
			PAGE_READWRITE,
			0,
			SHARED_MEMORY_WRITE_SIZE,
			FILE_MAPPING_NAME);
	}
	else
	{
#ifdef _DEBUG
		//MessageBox(NULL, "running", "warning", MB_OK);
#endif
		exit(0);
	}
}
