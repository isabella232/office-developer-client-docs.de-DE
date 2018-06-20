---
title: CharIndex-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Suchvorgänge gefunden ein Textausdruck für einen anderen Ausdruck und gibt dessen Start-positionieren, wenn.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790214"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex-Funktion (Access benutzerdefinierte Web app)

Suchvorgänge gefunden ein Textausdruck für einen anderen Ausdruck und gibt dessen Start-positionieren, wenn.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Ja  <br/> |Ein Ausdruck, der den gesuchten Text enthält.  <br/> |
| *WithinText*  <br/> |Ja  <br/> |Der Textausdruck, der durchsucht werden soll.  <br/> |
| *Start*  <br/> |Nein  <br/> |Eine ganze Zahl, die den Speicherort in *WithinText* zum Starten der Suche angibt. Wenn *Starten* nicht angegeben ist, eine negative Zahl ist oder 0 ist, beginnt die Suche am Anfang des *WithinText* .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn *TextExpression* oder *WithinText* NULL ist, gibt *CharIndex* NULL zurück. 
  
*TextExpression* in *WithinText*nicht gefunden wird, gibt *CharIndex* 0 zurück. 
  
Die Anfangsposition zurückgegeben ist 1-basierter, nicht 0-basiert.
  

