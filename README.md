# Escalonador-RoundRobin-C
Este código em C implementa um escalonador Round Robin. Ele lê detalhes dos processos de um arquivo, executa-os conforme o quantum definido e gera saídas. A função executeProcess gerencia a execução, enquanto a simulação continua até que todos os processos sejam concluídos.

Este código em C implementa um escalonador de processos usando o algoritmo Round Robin. Vou descrever as principais partes do código:

    Estrutura Process: Define uma estrutura para representar um processo. Cada processo possui um identificador (pid), duração, tempo de chegada, uma lista de tempos de I/O (ioTimes), contagem de operações de I/O (ioCount) e tempo restante para execução (remainingTime).

    Função executeProcess: Esta função é responsável por executar um processo por um quantum de tempo dado. Ela atualiza o tempo restante do processo, verifica se há operações de I/O a serem realizadas e imprime informações no arquivo de saída e no arquivo de gráfico de Gantt.

    Função main: Esta é a função principal do programa. Ela realiza as seguintes etapas:
        Lê o valor do quantum fornecido pelo usuário.
        Abre o arquivo de entrada que contém informações sobre os processos.
        Lê o número de processos e os detalhes de cada processo (pid, duração, tempo de chegada e tempos de I/O, se houver).
        Inicializa os arquivos de saída.
        Executa o escalonamento dos processos até que todos tenham sido concluídos.
        Imprime informações sobre o progresso da simulação, eventos de chegada, finalização de quantum e estado da fila de processos.
        Fecha os arquivos abertos e libera a memória alocada dinamicamente.

    Loop de execução: O escalonador funciona em um loop principal que avança o tempo e executa os processos. Ele continua até que todos os processos tenham sido concluídos.

    Geração de Saída: Durante a execução, o programa imprime informações importantes no console e em arquivos de saída, como eventos de chegada, operações de I/O, finalização de quantum e estado da fila de processos.

    Liberação de Memória: No final da execução, o código libera a memória alocada dinamicamente para os tempos de I/O de cada processo e para a lista de processos em si.
