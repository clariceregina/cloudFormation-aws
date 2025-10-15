# ☁️ AWS CloudFormation — Resumo

## 🧩 O que é o CloudFormation
O **AWS CloudFormation** é um serviço que permite **criar, provisionar e gerenciar infraestrutura AWS como código (IaC — Infrastructure as Code)**.  
Com ele, você define recursos da AWS em **templates declarativos** (YAML ou JSON), e o CloudFormation cuida do provisionamento automático e ordenado desses recursos.

---

## 🏗️ Conceitos Principais

### **Template**
- Arquivo em **YAML** ou **JSON** que descreve os recursos AWS.  
- Contém:
  - **Resources:** principais componentes (EC2, S3, VPC, etc.)
  - **Parameters:** entradas dinâmicas definidas pelo usuário
  - **Outputs:** valores retornados após a criação do stack
  - **Mappings:** tabelas estáticas de valores
  - **Conditions:** lógica condicional para criação de recursos

---

### **Stack**
- Uma **instância de um template**.
- Representa um **conjunto de recursos AWS criados e gerenciados juntos**.
- Pode ser:
  - **Criado:** provisiona os recursos.
  - **Atualizado:** aplica mudanças no template.
  - **Deletado:** remove todos os recursos associados.

---

### **Change Set**
- Permite **visualizar as mudanças** que serão aplicadas a um stack antes da execução.
- Importante para evitar impactos inesperados em produção.

---

## ⚙️ Fluxo de Funcionamento

1. **Crie o template** (YAML ou JSON) descrevendo a infraestrutura.  
2. **Envie o template** ao CloudFormation (via Console, CLI ou SDK).  
3. O CloudFormation **analisa dependências** e **provisiona recursos** em ordem correta.  
4. O serviço **mantém o estado** e permite **atualizações controladas**.

---

## 📦 Tipos de Templates

| Formato | Extensão | Vantagem |
|----------|-----------|-----------|
| JSON | `.json` | Compatibilidade e legibilidade por máquina |
| YAML | `.yaml` | Mais legível para humanos e suporta comentários |

---

## 🧠 Boas Práticas

- **Usar parâmetros** para tornar o template reutilizável.  
- **Versionar templates** (Git).  
- **Usar StackSets** para gerenciar múltiplas contas/regiões.  
- **Separar stacks** por domínio lógico (ex: rede, banco, aplicação).  
- **Usar Outputs** para exportar informações entre stacks.
