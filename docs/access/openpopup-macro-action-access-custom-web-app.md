---
title: OpenPopup-Makroaktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308113"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup-Makroaktion (Access Custom Web App)

Öffnet die angegebene Ansicht in einem Popupfenster.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Openpopup** (*View*, *Where =*, *Order by*) 
  
Die **openpopup** -Aktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *View*  <br/> |Der Name der zu öffnenden Ansicht.  <br/> |
| *WHERE =*  <br/> |Eine gültige SQL-WHERE-Klausel (ohne das Wort WHERE), die die Datensätze in der Ansicht einschränkt.  <br/> |
| *Sortiert nach*  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das aktuelle Makro endet, nachdem **** die openpopup-Aktion verarbeitet wurde. 
  
Alle vom Benutzer angewendeten Sortier-oder Filter Vorgänge werden gelöscht **** , wenn die openpopup-Aktion aufgerufen wird. 
  
Das *OrderBy* -Argument ist der Name der Felder, für die Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das *OrderBy* -Argument festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

