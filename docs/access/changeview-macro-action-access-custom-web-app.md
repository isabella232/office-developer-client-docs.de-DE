---
title: ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Sie können die ChangeView-Aktion verwenden, um zwischen Ansichten zu navigieren.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282313"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **ChangeView** -Aktion verwenden, um zwischen Ansichten zu navigieren. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **ChangeView** -Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|Tabelle  <br/> |Ja  <br/> |Der Name der zu öffnenden Tabelle.  <br/> |
|Ansicht  <br/> |Ja  <br/> |Der Name der zu öffnenden Ansicht.  <br/> |
|Dabei gilt:  <br/> |Nein  <br/> |Ersetzt die WHERE-Bedingung (sofern angegeben) der Objektdatenquelle.  <br/> |
|Sortiert nach  <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält. Dieses Argument ist standardmäßig leer.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Alle vom Benutzer angewendeten Sortier-oder Filter Vorgänge werden gelöscht, wenn die **ChangeView** -Aktion aufgerufen wird. 
  
Das *OrderBy* -Argument ist der Name der Felder, für die Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). 
  
Wenn Sie das *OrderBy* -Argument festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert. 
  

