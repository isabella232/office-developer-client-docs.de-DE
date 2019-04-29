---
title: CharIndex-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, falls gefunden.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423132"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex-Funktion (Access Custom Web App)

Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, falls gefunden.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**CHARINDEX** (*Text*-, *WithinText*-, [*Start*]) 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *Text*  <br/> |Ja  <br/> |Ein Textausdruck, der den gefundenen Text enthält.  <br/> |
| *WithinText*  <br/> |Ja  <br/> |Der Textausdruck, der durchsucht werden soll.  <br/> |
| *Start*  <br/> |Nein  <br/> |Eine ganze Zahl, die den Speicherort in *WithinText* angibt, an dem die Suche beginnen soll. Wenn *Start* nicht angegeben ist, eine negative Zahl ist oder 0 ist, beginnt die Suche am Anfang von *WithinText* .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Text* -oder *WithinText* ist, gibt *CHARINDEX* NULL zurück. 
  
Wenn *Textform* in *WithinText*nicht gefunden wird, gibt *CHARINDEX* 0 zurück. 
  
Die zurückgegebene Startposition ist 1-basiert, nicht 0-basiert.
  

