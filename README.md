# Explorando o MINIX 3 - System Call `get_mem_usage()`

Implementação de uma chamada de sistema nativa (`get_mem_usage()`) no sistema operacional baseado em microkernel **MINIX 3** e validação experimental por meio de um programa de usuário em C.

> **Instituição:** Universidade do Estado do Rio Grande do Norte (UERN)  
> **Curso:** Bacharelado em Ciência da Computação  
> **Disciplina:** Sistemas Operacionais - 3ª Unidade  
> **Tema:** `get_mem_usage()` - Retorna a quantidade de memória física livre no sistema (em KB)

---

## Sumário

- [Sobre o Projeto](#sobre-o-projeto)

---

## Sobre o Projeto

O objetivo deste trabalho é compreender na prática o funcionamento interno de um sistema operacional de arquitetura microkernel, percorrendo todas as camadas envolvidas no atendimento de uma chamada de sistema no MINIX 3.3.0:

1. Instalação e configuração do MINIX 3 em máquina virtual;
2. Obtenção do código-fonte e recompilação bem-sucedida do kernel original;
3. Registro e implementação da nova chamada de sistema `get_mem_usage()` no **Process Manager (PM)**, integrando-a ao **Virtual Memory Server (VM)**;
4. Exposição da interface na biblioteca padrão C (**libc**) e em `<unistd.h>`;
5. Desenvolvimento de um programa em C no *User Space* (`test_mem_usage.c`) para validar a chamada em tempo real com alocação dinâmica de memória e verificação cruzada com `/proc/meminfo`.
