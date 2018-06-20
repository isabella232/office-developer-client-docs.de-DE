---
title: OpenPopup-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790329"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup-Makroaktion (Access benutzerdefinierte Web app)

Öffnet die angegebene Ansicht in einem Popupfenster.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **OpenPopup** (*Anzeigen*, *, in dem =*, *der Order By*) 
  
Die **OpenPopup** -Aktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *View*  <br/> |Der Name der Ansicht zu öffnen.  <br/> |
| *Wobei =*  <br/> |Eine gültige SQL WHERE-Klausel (ohne das Wort, in dem), die die Datensätze in der Ansicht beschränkt.  <br/> |
| *Sortiert nach*  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Standardmäßig ist dieses Argument leer.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das aktuelle Makro beendet, sobald die Aktion **OpenPopup** verarbeitet wird. 
  
Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **OpenPopup** aufgerufen wird. 
  
Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

