---
title: Fürjedendatensatz-Daten Block (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Ein Fürjedendatensatz-Datenblock wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302457"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Fürjedendatensatz-Daten Block (Access Custom Web App)

Ein **fürjedendatensatz** -Datenblock wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**In** <br/> |Ja  <br/> |Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll. Das Argument *in* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL-Anweisung enthalten.  <br/> **Hinweis**: die angegebene Domäne kann Daten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind, nicht aufnehmen.           |
|**Bedingung** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, mit dem der Datenumfang eingeschränkt wird, auf dem der **fürjedendatensatz** -Datenblock ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien ausgelassen werden, wird der **fürjedendatensatz** -Datenblock auf die gesamte Domäne angewendet, die durch das *in* -Argument angegeben wird. Jedes Feld, das in Criteria enthalten ist, muss auch ein Feld in *in* sein.  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für die durch das Argument *in* angegebene Domäne bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn *Alias* nicht angegeben wird, wird der Tabellen-oder Abfragename als Alias verwendet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort. 
  

