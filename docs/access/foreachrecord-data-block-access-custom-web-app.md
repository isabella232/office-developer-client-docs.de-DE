---
title: ForEachRecord-Datenblock (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Ein ForEachRecord-Datenblock wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne.
ms.openlocfilehash: 65c87cfd44796d16310c38da303dfcd3c7c81384
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601541"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord-Datenblock (benutzerdefinierte Access-Web-App)

Ein **ForEachRecord-Datenblock** wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**In** <br/> |Ja  <br/> |Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll. Das Argument *"In"* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL Anweisung enthalten.  <br/> **HINWEIS:** Die angegebene Domäne kann keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.           |
|**Bedingung** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der **ForEachRecord-Datenblock** ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der **ForEachRecord-Datenblock** für die gesamte durch das  *Argument "In"*  angegebene Domäne ausgeführt. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in  *In*  sein.  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für die durch das  *Argument "In"*  angegebene Domäne bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn  *alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort. 
  

