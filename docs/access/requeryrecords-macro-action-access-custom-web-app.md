---
title: Erneutabfragendatensätze-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Sie können die Erneutabfragendatensätze-Aktion verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut Abfragen.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439247"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Erneutabfragendatensätze-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **erneutabfragendatensätze** -Aktion verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut Abfragen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **erneutabfragendatensätze** -Aktion hat die folgenden Argumente. 
  
|**Parameter**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**WHERE =** <br/> |Nein  <br/> |Eine SQL-WHERE-Klausel, die die Datensätze in der Ansicht einschränkt. Dieses Argument ist standardmäßig leer.  <br/> |
|**OrderBy** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Alle vom Benutzer angewendeten Sortier-oder Filter Vorgänge werden gelöscht, wenn die **erneutabfragendatensätze** -Aktion aufgerufen wird. 
  
Das *OrderBy* -Argument ist der Name der Felder, für die Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das *OrderBy* -Argument festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  
Um Datensätze in absteigender Reihenfolge zu sortieren, geben Sie DESC am Ende des Argumentausdrucks *OrderBy* ein. Wenn Sie beispielsweise Kundendatensätze in absteigender Reihenfolge nach dem Namen des Kontakts sortieren möchten, legen Sie das *OrderBy* -Argument auf "ContactName DESC" fest. 
  
Zum Sortieren von Namen nach LastName absteigend und FirstName aufsteigend legen Sie das *OrderBy* -Argument auf "LastName DESC, FirstName ASC" fest. 
  

