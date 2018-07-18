---
title: ChangeView-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Die ChangeView-Aktion können Sie um zwischen Ansichten direkt zu navigieren.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790208"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView-Makroaktion (Access benutzerdefinierte Web app)

Die **ChangeView** -Aktion können Sie um zwischen Ansichten direkt zu navigieren. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **ChangeView** -Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|Tabelle  <br/> |Ja  <br/> |Der Name der zu öffnenden Tabelle.  <br/> |
|Ansicht  <br/> |Ja  <br/> |Der Name der Ansicht zu öffnen.  <br/> |
|Wobei  <br/> |Nein  <br/> |Ersetzt, wenn angegeben, die Bedingung der Datensatzquelle des Objekts.  <br/> |
|Sortiert nach  <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält. Standardmäßig ist dieses Argument leer.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **ChangeView** aufgerufen wird. 
  
Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

