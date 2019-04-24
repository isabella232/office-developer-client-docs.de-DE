---
title: Round-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen abgerundeten oder abgeschnittenen numerischen Wert auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307959"
---
# <a name="round-function-access-custom-web-app"></a>Round-Funktion (Access Custom Web App)

Gibt einen abgerundeten oder abgeschnittenen numerischen Wert auf die angegebene Länge oder Genauigkeit zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Round** (*Anzahl*, *Genauigkeit* , [ *TruncateInsteadOfRound* ]) 
  
Die **Round** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Number*  <br/> |Ein numerischer Ausdruck.  <br/> |
| *Genauigkeit*  <br/> |Die Genauigkeit, mit der die *Zahl* gerundet werden soll.  Bei der *Genauigkeit* muss es sich um einen numerischen Ausdruck handeln. Wenn die *Genauigkeit* eine positive Zahl ist, wird *Zahl* auf die Anzahl der durch length angegebenen Dezimalstellen gerundet. Wenn die *Genauigkeit* eine negative Zahl ist, wird die *Zahl* auf der linken Seite des Dezimalkommas, wie durch length angegeben, gerundet.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Der Typ des auszuführenden Vorgangs. Wenn der Wert nicht angegeben oder auf 0 festgelegt ist, wird *Zahl* gerundet. Wenn ein anderer Wert als 0 angegeben wird, wird *Number* abgeschnitten. Der Standardwert ist 0.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **Round** gibt immer einen Wert zurück. Wenn length negativ und größer als die Anzahl der Ziffern vor dem Dezimaltrennzeichen ist, gibt **Round** den Wert 0 zurück. 
  

