---
title: OpenPopup-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427388"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup-Makroaktion (benutzerdefinierte Access-Web-App)

Öffnet die angegebene Ansicht in einem Popupfenster.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
Die **OpenPopup-Aktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *View*  <br/> |Der Name der zu öffnende Ansicht.  <br/> |
| *Where=*  <br/> |Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE), die die Datensätze in der Ansicht einschränkt.  <br/> |
| *Sortiert nach*  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Standardmäßig ist dieses Argument leer.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das aktuelle Makro endet, nachdem die **OpenPopup-Aktion** verarbeitet wurde. 
  
Alle vom Benutzer angewendeten Sortierungen oder Filter werden beim **ÖffnenPopup-Aktionsvorgang** geleert. 
  
Das  *OrderBy-Argument*  ist der Name des Felds oder der Felder, nach denen Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das  *Argument OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

