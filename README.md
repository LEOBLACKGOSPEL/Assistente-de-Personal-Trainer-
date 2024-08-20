# Assistente-de-Personal-Trainer-
Assistente de Personal Trainer - Gerador de Treino Ideal
class PlanoTreino:
    def __init__(self, biotipo, dias_por_semana, tipo_exercicio):
        self.biotipo = biotipo
        self.dias_por_semana = dias_por_semana
        self.tipo_exercicio = tipo_exercicio

    def gerar_plano(self):
        plano = f"Plano de Treino para {self.biotipo}:\n"
        plano += f"Treinos por semana: {self.dias_por_semana}\n\n"
        
        if self.tipo_exercicio == 'Funcional':
            plano += "Treino Funcional:\n"
            plano += "- Agachamentos\n"
            plano += "- Flexões\n"
            plano += "- Pranchas\n"
            plano += "- Lunges\n"
        
        elif self.tipo_exercicio == 'Maquinário':
            plano += "Treino com Maquinário:\n"
            plano += "- Leg Press\n"
            plano += "- Pec Deck\n"
            plano += "- Pulldown\n"
            plano += "- Cadeira Extensora\n"
        
        elif self.tipo_exercicio == 'Peso Livre':
            plano += "Treino com Peso Livre:\n"
            plano += "- Supino\n"
            plano += "- Remada com Barra\n"
            plano += "- Agachamento com Barra\n"
            plano += "- Desenvolvimento com Halteres\n"
        
        elif self.tipo_exercicio == 'Cardio':
            plano += "Treino Cardio:\n"
            plano += "- Corrida\n"
            plano += "- Ciclismo\n"
            plano += "- Natação\n"
            plano += "- Pular Corda\n"
        
        elif self.tipo_exercicio == 'HIIT':
            plano += "Treino HIIT:\n"
            plano += "- Burpees\n"
            plano += "- Saltos\n"
            plano += "- Sprints\n"
            plano += "- Mountain Climbers\n"
        
        else:
            plano += "Tipo de exercício não reconhecido. Por favor, escolha um tipo válido.\n"
        
        return plano

# Exemplo de uso
biotipo = 'Mesomorfo'  # Pode ser 'Ectomorfo', 'Mesomorfo', ou 'Endomorfo'
dias_por_semana = 4
tipo_exercicio = 'Peso Livre'  # Pode ser 'Funcional', 'Maquinário', 'Peso Livre', 'Cardio', ou 'HIIT'

plano = PlanoTreino(biotipo, dias_por_semana, tipo_exercicio)
print(plano.gerar_plano())
