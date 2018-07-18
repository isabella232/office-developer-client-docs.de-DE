---
title: RequeryRecords-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Sie können die RequeryRecords-Aktion verwenden, aktualisieren, Sortieren und Filtern der Daten in der aktiven Ansicht durch erneutes Abfragen der Quelle der Ansicht.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790347"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords-Makroaktion (Access benutzerdefinierte Web app)

Sie können die **RequeryRecords** -Aktion verwenden, aktualisieren, Sortieren und Filtern der Daten in der aktiven Ansicht durch erneutes Abfragen der Quelle der Ansicht. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **RequeryRecords** -Aktion hat die folgenden Argumente. 
  
|**Parameter**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Wobei =** <br/> |Nein  <br/> |Eine SQL WHERE-Klausel, die die Datensätze in der Ansicht beschränkt. Standardmäßig ist dieses Argument leer.  <br/> |
|**OrderBy** <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Standardmäßig ist dieses Argument leer.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **RequeryRecords** aufgerufen wird. 
  
Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  
Geben Sie DESC am Ende des Ausdrucks-Argument *OrderBy* , um Datensätze in absteigender Reihenfolge zu sortieren. Legen Sie beispielsweise Kundendatensätze in absteigender Reihenfolge nach dem Namen des Kontakts, um das Argument *OrderBy* "ContactName DESC". 
  
Um die Namen von absteigender LastName und FirstName Aufsteigend sortieren, legen Sie das Argument *OrderBy* auf "DESC LastName, FirstName ASC". 
  

