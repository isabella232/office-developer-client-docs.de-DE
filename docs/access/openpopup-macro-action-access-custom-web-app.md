---
title: ÖffnenPopup-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: f381389dad13e2a31fa73009118804ed5588c048
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576814"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>ÖffnenPopup-Makroaktion (benutzerdefinierte Access-Web-App)

Öffnet die angegebene Ansicht in einem Popupfenster.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
Die **OpenPopup-Aktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *View*  <br/> |Der Name der zu öffnenden Ansicht.  <br/> |
| *Where=*  <br/> |Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE), die die Datensätze in der Ansicht einschränkt.  <br/> |
| *Sortiert nach*  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das aktuelle Makro wird beendet, nachdem die **OpenPopup-Aktion** verarbeitet wurde. 
  
Alle vom Benutzer angewendeten Sortierungen oder Filterungen werden gelöscht, wenn die **OpenPopup-Aktion** aufgerufen wird. 
  
Das  *Argument OrderBy*  ist der Name des Felds oder der Felder, nach denen Datensätze sortiert werden sollen. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument  *OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

