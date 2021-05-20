---
title: ForEachRecord Data Block (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Ein ForEachRecord-Datenblock wiederholt einen Satz von Anweisungen für jeden Datensatz in einer Domäne.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428235"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord Data Block (benutzerdefinierte Access-Web-App)

Ein **ForEachRecord-Datenblock** wiederholt einen Satz von Anweisungen für jeden Datensatz in einer Domäne. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**In** <br/> |Ja  <br/> |Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll. Das *Argument In* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL enthalten.  <br/> **HINWEIS**: Die angegebene Domäne darf keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.           |
|**Bedingung** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der **ForEachRecord-Datenblock** ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der **ForEachRecord-Datenblock** für die gesamte Domäne ausgeführt, die durch das  *Argument In angegeben*  wird. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in *sein.*  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für die durch das  *Argument In*  angegebene Domäne enthält. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn  *Alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort. 
  

