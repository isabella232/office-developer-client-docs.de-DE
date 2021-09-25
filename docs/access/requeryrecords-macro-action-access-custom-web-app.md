---
title: RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Mit der Aktion "ErneutabfrageDatensätze" können Sie die Daten in der aktiven Ansicht aktualisieren, sortieren und filtern, indem Sie die Quelle der Ansicht erneut abfragen.
ms.openlocfilehash: bbfd4f2738e7e2dcb46346c83ea0804b8bd7b8b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552367"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der Aktion **"ErneutabfrageDatensätze"** können Sie die Daten in der aktiven Ansicht aktualisieren, sortieren und filtern, indem Sie die Quelle der Ansicht erneut abfragen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **Aktion "RequeryRecords"** hat die folgenden Argumente. 
  
|**Parameter**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Where=** <br/> |Nein  <br/> |Eine SQL WHERE-Klausel, die die Datensätze in der Ansicht einschränkt. Dieses Argument ist standardmäßig leer.  <br/> |
|**OrderBy** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Alle vom Benutzer angewendeten Sortierungen oder Filterungen werden gelöscht, wenn die **RequeryRecords-Aktion** aufgerufen wird. 
  
Das  *Argument OrderBy*  ist der Name des Felds oder der Felder, nach denen Datensätze sortiert werden sollen. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument  *OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  
Um Datensätze in absteigender Reihenfolge zu sortieren, geben Sie DESC am Ende des Argumentausdrucks  *OrderBy*  ein. Um beispielsweise Kundendatensätze in absteigender Reihenfolge nach Kontaktnamen zu sortieren, legen Sie das Argument  *OrderBy*  auf "ContactName DESC" fest. 
  
Um Namen nach absteigender Nachname und aufsteigender Reihenfolge nach Vorname zu sortieren, legen Sie das Argument  *OrderBy*  auf "LastName DESC, FirstName ASC" fest. 
  

