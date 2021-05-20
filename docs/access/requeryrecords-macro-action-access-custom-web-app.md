---
title: RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Sie können die RequeryRecords-Aktion verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut anzeigen.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439247"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **RequeryRecords-Aktion** verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut anzeigen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **RequeryRecords-Aktion** hat die folgenden Argumente. 
  
|**Parameter**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Where=** <br/> |Nein  <br/> |Eine SQL WHERE-Klausel, die die Datensätze in der Ansicht einschränkt. Standardmäßig ist dieses Argument leer.  <br/> |
|**OrderBy** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält. Standardmäßig ist dieses Argument leer.  <br/> |
   
## <a name="remarks"></a>Hinweise

Alle vom Benutzer angewendeten Sortierungen oder Filterungen werden beim Aufgerufen der **RequeryRecords-Aktion** geleert. 
  
Das  *OrderBy-Argument*  ist der Name des Felds oder der Felder, nach denen Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das  *Argument OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  
Um Datensätze in absteigender Reihenfolge zu sortieren, geben Sie DESC am Ende des  *OrderBy-Argumentausdrucks*  ein. Wenn Sie z. B. Kundendatensätze in absteigender Reihenfolge nach Kontaktnamen sortieren möchten, legen Sie das  *Argument OrderBy*  auf "ContactName DESC" festgelegt. 
  
Zum Sortieren von Namen nach dem absteigenden LastName und dem aufsteigenden FirstName-Argument legen Sie  *das OrderBy-Argument*  auf "LastName DESC, FirstName ASC" ein. 
  

