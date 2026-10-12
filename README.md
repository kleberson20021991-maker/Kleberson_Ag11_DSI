from colorama import Fore, Style, init

init(autoreset=True)

niveis_reservatorio = [
    {"nivel": 1, "situacao": "Muito baixo (crítico)", "cor": Fore.RED},
    {"nivel": 2, "situacao": "Baixo", "cor": Fore.YELLOW},
    {"nivel": 3, "situacao": "Médio", "cor": Fore.GREEN},
    {"nivel": 4, "situacao": "Alto", "cor": Fore.CYAN},
    {"nivel": 5, "situacao": "Muito alto (alerta)", "cor": Fore.BLUE},
]


def exibir_alerta(nivel, situacao, cor):
  print(
      f"{cor}[MONITORAMENTO] Nível {nivel} do Reservatório: {situacao}"
      f" {Style.RESET_ALL}"
  )


def simular_monitoramento():
  print("=== INICIANDO SIMULAÇÃO DE NÍVEIS DE ÁGUA ===")
  print("-" * 50)
  for item in niveis_reservatorio:
    exibir_alerta(item["nivel"], item["situacao"], item["cor"])
  print("-" * 50)
  print("Simulação concluída. Estilo padrão do terminal restaurado.")


if __name__ == "__main__":
  simular_monitoramento()

