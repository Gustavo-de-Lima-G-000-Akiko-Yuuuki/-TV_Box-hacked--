
# TV Box: Unbrick & Unlock 

Basicamente um repositório com os arquivos que usei em um serviço que peguei para consertar uma TV Box "brikada" e fazer o desbloqueio para remover a mensalidade. Não vou me estender muito pois foi um serviço rápido (umas 6 horas de trampo e muito Monster). Qualquer coisa avisa.

![Banner](https://raw.githubusercontent.com/SEU-USUARIO/TV-BOX-ARQUIVOS-REFERENCIAS/main/assets/banner.png)

---

## Estrutura do Repositório

Não organizei arquivos, mas prete a atenção quando fazer o flash:

```text
Não Vou organizaar mas se quiser ajuda ok 
```

## Ferramentas de Flash e Recovery

Dependendo do chipset da sua box, você vai precisar de um software específico. As principais ferramentas que utilizei/recomendo estão listadas abaixo:

| Ferramenta | Chipset Alvo | Uso Principal |
|---|---|---|
| **Amlogic USB Burning Tool** | Amlogic | Flash de firmware oficial e custom |
| **RKDevTool** | Rockchip | Recuperação e gravação de imagem |
| **SP Flash Tool** | MediaTek | Unbrick e flash de partições |
| **ADB & Fastboot** | Universal | Debugging, sideload de ROMs e acesso shell |
| **Magisk** | Universal | Root e injeção de módulos |

## Fontes e Referências (Onde caçar arquivos)

Se a sua placa for diferente, você vai precisar caçar a ROM específica. Os melhores lugares que usei como base foram:

**Comunidades e ROMs:**
* [4PDA](https://4pda.to/forum/) *(Fórum russo, essencial. Use o tradutor do navegador)*
* [XDA Developers](https://forum.xda-developers.com/)
* [SlimBOX TV](https://slimboxtv.ru/) *(Ótimas ROMs customizadas)*
* [ATV Experience](https://www.atvxperience.com/)

**Repositórios de APKs (Mods/Lite):**
* [Modyolo](https://modyolo.com/) | [LiteAPKs](https://liteapks.com/) | [APKDone](https://apkdone.com/)

---

## Resumo do Procedimento de Flash

Caso precise de um guia rápido de como procedi via ADB/Recovery:

**1. Ativar Debug USB**
Vá em `Configurações > Sobre > Número da versão` (clique 7 vezes). 
Depois vá em `Sistema > Opções de Desenvolvedor` e ative o Debug USB.

**2. Entrar no Recovery**
Geralmente feito segurando o botão de reset (dentro da entrada AV) enquanto liga na energia, ou via terminal:
```bash
adb reboot recovery
```

**3. Flash / Sideload**
Com o cabo USB macho-macho conectado e os drivers instalados:
```bash
adb sideload nome_da_rom.zip
```

> **Atenção redobrada:** 
> Antes de flashear qualquer coisa, abra a sua TV Box e olhe a placa mãe. Identifique exatamente o **Chipset** (Amlogic, Rockchip, Allwinner) e o **módulo de Wi-Fi**. Flashear uma ROM com o driver de Wi-Fi errado vai deixar sua box sem internet. Faça o dump da ROM original sempre que possível. Nunca desligue a fonte de energia durante o processo.

---

## Contribuições

Se tiver alguma ROM braba, algum script de debloat ou APK que salva a vida, sinta-se livre para abrir um Pull Request.

```bash
git clone https://github.com/SEU-USUARIO/TV-BOX-ARQUIVOS-REFERENCIAS.git
```

**Licença:** MIT
```

***

### O que mudou:
1. **Visual mais limpo:** Troquei o excesso de emojis por blocos de texto (`text` e `bash`), que deixam o GitHub muito mais profissional e com cara de repositório de código.
2. **Tom de voz:** Adaptei as instruções para parecerem anotações de um técnico/modder ("onde caçar arquivos", "atenção redobrada", "olhe a placa mãe").
3. **Fim da repetição:** A IA havia feito listas enormes com links espalhados. Juntei tudo em blocos mais coesos para facilitar a leitura.
