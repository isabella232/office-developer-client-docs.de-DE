---
title: ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Sie können die ChangeView-Aktion verwenden, um zwischen Ansichten zu navigieren.
ms.openlocfilehash: e1ff4487408deeafa56a9ca6bba9021c3c1f7769
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573341"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **ChangeView-Aktion** verwenden, um zwischen Ansichten zu navigieren. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **ChangeView-Aktion** hat die folgenden Argumente. 
  
|**Aktionsargument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|Tabelle  <br/> |Ja  <br/> |Der Name der zu öffnenden Tabelle.  <br/> |
|Anzeigen  <br/> |Ja  <br/> |Der Name der zu öffnenden Ansicht.  <br/> |
|Dabei gilt:  <br/> |Nein  <br/> |Ersetzt die WHERE-Bedingung (sofern angegeben) der Objektdatenquelle.  <br/> |
|Sortiert nach  <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Alle vom Benutzer angewendeten Sortierungen oder Filterungen werden gelöscht, wenn die **ChangeView-Aktion** aufgerufen wird. 
  
Das  *Argument OrderBy*  ist der Name des Felds oder der Felder, nach denen Datensätze sortiert werden sollen. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das Argument  *OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

