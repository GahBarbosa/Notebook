O Amazon EC2 é compatível com os seguintes hipervisores: Xen e Nitro.

###### Uso geral 
As instâncias de uso geral fornecem um equilíbrio entre recursos de computação, memória e rede. Essas instâncias são ideais para aplicações que usam esses recursos em proporções iguais, como servidores Web e repositórios de código.
###### Otimizadas para memória
As instâncias otimizadas na memória são projetadas para fornecer performance rápida para workloads que processam grandes bancos de dados na memória.

###### Otimizadas para armazenamento
As instâncias otimizadas para armazenamento foram projetadas para workloads que exijam acesso sequencial de leitura e gravação a conjuntos de dados muito grandes no armazenamento local. Elas são otimizadas para fornecer dezenas de milhares de baixa latência, operações de E/S aleatórias por segundo (IOPS) para aplicações.

###### Computação acelerada
As instâncias de computação acelerada usam aceleradores de hardware, ou coprocessadores, para executar funções, como cálculos de números de ponto flutuante, processamento gráfico ou correspondência de padrões de dados, com mais eficiência do que é possível em software executado. 

###### Com computação de alta performance
As instâncias de computação de alto desempenho foram criadas especificamente para oferecer a melhor relação preço/desempenho para executar cargas de trabalho de HPC em grande escala. AWS Essas instâncias são ideais para aplicações que se beneficiam de processadores de alto desempenho, como simulações grandes e complexas e workloads de aprendizado profundo.
###### Instâncias baseadas em Nitro

- **Uso geral**: M5 | M5a | M5ad | M5d | M5dn | M5n | M5zn | M6a | M6g | M6gd | M6i | M6id | M6idn | M6in | M7a | M7g | M7gd | M7i | M7i-flex | M8g | T3 | T3a | T4g
- **Otimizadas para computação**: C5 | C5a | C5ad | C5d | C5n | C6a | C6g | C6gd | C6gn | C6i | C6id | C6in | C7a | C7g | C7gd | C7gn | C7i | C7i-flex | C8g
- **Otimizadas para memória**: R5 | R5a | R5ad | R5b | R5d | R5dn | R5n | R6a | R6g | R6gd | R6i | R6idn | R6in | R6id | R7a | R7g | R7gd | R7i | R7iz | R8g | U-3tb1 | U-6tb1 | U-9tb1 | U-12tb1 | U-18tb1 | U-24tb1 | U7i-6tb | U7i-8tb | U7i-12tb | U7in-16tb | U7in-24tb | U7in-32tb | U7inh-32tb | X2gd | X2idn | X2iedn | X2iezn | X8g | z1d
- **Otimizadas para armazenamento**: D3 | D3en | I3en | I4g | I4i | I7ie | I8g | Im4gn | Is4gen
- **Computação acelerada**: DL1 | DL2q | F2 | G4ad | G4dn | G5 | G5g | G6 | G6e | Gr6 | Inf1 | Inf2 | P3dn | P4d | P4de | P5 | P5e | P5en | Trn1 | Trn1n | Trn2 | Trn2u | VT1
- **Com computação de alta performance**: Hpc6a | Hpc6id | Hpc7a | Hpc7g

###### Instâncias baseadas em Xen

- **Uso geral**: M1 | M2 | M3 | M4 | T1 | T2
- **Otimizadas para computação**: C1 | C3 | C4
- **Otimizadas para memória**: R3 | R4 | X1 | X1e
- **Otimizadas para armazenamento**: D2 | H1 | I2 | I3
- **Computação acelerada**: F1 | G3 | P2 | P3

**Para obter mais informações sobre as versões compatíveis do hipervisor Nitro, consulte [Network feature support](https://docs.aws.amazon.com/ec2/latest/instancetypes/ec2-nitro-instances.html#nitro-version-network-features) no _Guia de tipos de instâncias do Amazon EC2_.
