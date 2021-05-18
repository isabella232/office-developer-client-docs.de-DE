---
title: Round-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen numerischen Wert( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413745"
---
# <a name="round-function-access-custom-web-app"></a>Round-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen numerischen Wert( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ]) 
  
Die **Round-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Number*  <br/> |Ein numerischer Ausdruck.  <br/> |
| *Genauigkeit*  <br/> |Die Genauigkeit, auf die  *Number*  gerundet werden soll.  *Genauigkeit*  muss ein numerischer Ausdruck sein. Wenn  *Precision*  eine positive Zahl ist, wird  *Number*  auf die Anzahl der dezimalen Positionen gerundet, die durch die Länge angegeben sind. Wenn  *Precision*  eine negative Zahl ist, wird  *Number*  auf der linken Seite des Dezimalkomma gerundet, wie durch die Länge angegeben.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Der Typ des durchzuführende Vorgangs. Wenn sie nicht angegeben oder auf 0 festgelegt ist,  *wird Number*  gerundet. Wenn ein anderer Wert als 0 angegeben wird, wird  *Number*  abgeschnitten. Der Standardwert ist 0.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Round** gibt immer einen Wert zurück. Wenn die Länge negativ und größer als die Anzahl der Ziffern vor dem Dezimalkomma ist, gibt **Round** 0 zurück. 
  

