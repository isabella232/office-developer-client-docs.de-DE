---
title: FürJedenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Mit einem FürJedenDatensatz-Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790213"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>FürJedenDatensatz-Datenblock (Access benutzerdefinierte Web app)

Mit einem **FürJedenDatensatz** -Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> [!HINWEIS] Der **FürJedenDatensatz** -Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **FürJedenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**In** <br/> |Ja  <br/> |Eine Zeichenfolge zur Identifizierung von Datensätzen für den Betrieb die Domäne. Das *im* Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.  <br/> **Hinweis**: die angegebene Domäne darf keine enthalten Daten in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.           |
|**Where Condition** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des **FürJedenDatensatz** -Datenblocks wird ausgeführt. Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem. Wenn Kriterien Length angegeben werden, wirkt sich auf die gesamte Domäne, die durch das Argument *im* angegebenen **FürJedenDatensatz** -Datenblock. Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in *In* sein.  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für die Domäne, die durch das Argument *im* angegebenen bereitstellt. Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen. Wenn *Alias* nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort. 
  

