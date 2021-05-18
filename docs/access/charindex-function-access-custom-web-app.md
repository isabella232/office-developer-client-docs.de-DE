---
title: CharIndex-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, wenn er gefunden wird.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423132"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex-Funktion (benutzerdefinierte Access-Web-App)

Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, wenn er gefunden wird.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Ja  <br/> |Ein Textausdruck, der den zu findende Text enthält.  <br/> |
| *WithinText*  <br/> |Ja  <br/> |Der zu durchsuchende Textausdruck.  <br/> |
| *Start*  <br/> |Nein  <br/> |Eine ganze Zahl, die den Speicherort in  *WithinText angibt,*  um mit der Suche zu beginnen. Wenn  *Start*  nicht angegeben ist, eine negative Zahl oder 0 ist, beginnt die Suche am Anfang von  *WithinText*  .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn  *TextExpression oder*  *WithinText*  NULL ist,  *gibt CharIndex*  NULL zurück. 
  
Wenn  *TextExpression*  nicht in  *WithinText* gefunden wird, gibt  *CharIndex*  0 zurück. 
  
Die zurückgegebene Ausgangsposition ist 1-basiert und nicht 0-basiert.
  

