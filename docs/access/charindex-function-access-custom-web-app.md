---
title: CharIndex-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Anfangsposition zurück, wenn er gefunden wird.
ms.openlocfilehash: bd0b14210a4e4ac73cbbca6198fa86d823853f88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577717"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex-Funktion (benutzerdefinierte Access-Web-App)

Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Anfangsposition zurück, wenn er gefunden wird.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Ja  <br/> |Ein Textausdruck, der den zu findenden Text enthält.  <br/> |
| *WithinText*  <br/> |Ja  <br/> |Der zu durchsuchende Textausdruck.  <br/> |
| *Start*  <br/> |Nein  <br/> |Eine ganze Zahl, die die Position in  *WithinText*  angibt, an der die Suche beginnen soll. Wenn  *Start*  nicht angegeben ist, eine negative Zahl oder 0 ist, beginnt die Suche am Anfang von  *WithinText*  .  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  *TextExpression*  oder  *WithinText*  NULL ist, gibt  *CharIndex*  NULL zurück. 
  
Wenn  *TextExpression*  in  *WithinText* nicht gefunden wird, gibt  *CharIndex*  0 zurück. 
  
Die zurückgegebene Startposition ist 1- und nicht 0-basiert.
  

