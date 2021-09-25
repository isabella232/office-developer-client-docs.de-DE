---
title: Round-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen numerischen Wert ( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: e974cecbc2f602af12ba7aa572541c2f9bee319f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593068"
---
# <a name="round-function-access-custom-web-app"></a>Round-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen numerischen Wert ( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Round** (*Number*, *Precision*  , [  *TruncateIn flyOfRound*  ]) 
  
Die **Round-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Number*  <br/> |Ein numerischer Ausdruck.  <br/> |
| *Präzision*  <br/> |Die Genauigkeit, auf die  *Zahl*  gerundet werden soll.  *Die Genauigkeit*  muss ein numerischer Ausdruck sein. Wenn  *Genauigkeit*  eine positive Zahl ist, wird  *Zahl*  auf die Anzahl der Dezimalstellen gerundet, die durch die Länge angegeben sind. Wenn *Genauigkeit* eine negative Zahl ist, wird Zahl auf der linken Seite des Dezimalpunkts gerundet, wie durch die Länge angegeben.   <br/> |
| *TruncateIn flyOfRound*  <br/> |Der Auszuführende Vorgangstyp. Wenn Zahl weggelassen oder auf 0 festgelegt wird, wird  *Zahl*  gerundet. Wenn ein anderer Wert als 0 angegeben wird, wird  *Zahl*  abgeschnitten. Der Standardwert ist 0.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **Round** gibt immer einen Wert zurück. Wenn die Länge negativ und größer als die Anzahl der Ziffern vor dem Dezimalkomma ist, gibt **Round** 0 zurück. 
  

