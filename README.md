O termo Localização refere-se ao processo de adaptar um aplicativo para funcionar em diferentes culturas e regiões

Na plataforma .NET a localização em geral  é feita usando recursos (resources) que podem incluir arquivos texto simples,
arquivos XML ou bancos de dados que contêm as traduções de textos e outras informações necessárias para a localização

O roteiro para realizar a localização pode ser descrito de forma resumida da seguinte forma

- Configurar serviços de localização incluindo o pacote nuget : Microsoft.Extensions.Localization
- Criar os arquivos de recursos (.resx) no projeto para cada idioma que desejamos suportar : Resources.en-US.resx , Resources.pt-BR.resx
  onde definimos o nome seguido do identificador de cultura em duas partes o identificador do idioma e o identificador do pais
  en-US se refere ao inglês nos Estados Unidos.
- Adicionar os textos que desejamos localizar nos arquivos de recursos (XML) : formato : chave - valor
- Usar os textos localizados nas páginas razor usando a interface  IStringLocalizer para obter as strings localizadas dos arquivos de recursos : 
  Ex: IStringLocalizer<Resources> localizer
- Alternar a cultura para testar as diferentes culturas configuradas



