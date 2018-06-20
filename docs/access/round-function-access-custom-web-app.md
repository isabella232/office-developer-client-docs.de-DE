---
title: Round-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen numerischen Wert, entweder gerundet oder abgeschnitten werden, auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790358"
---
# <a name="round-function-access-custom-web-app"></a>Round-Funktion (Access benutzerdefinierte Web app)

Gibt einen numerischen Wert, entweder gerundet oder abgeschnitten werden, auf die angegebene Länge oder Genauigkeit zurück.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Round** (*Anzahl*, *Precision* , [ *TruncateInsteadOfRound* ]) 
  
Die **Round** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Number*  <br/> |Ein numerischer Ausdruck.  <br/> |
| *Mit doppelter Genauigkeit*  <br/> |Die Genauigkeit an die *Zahl* gerundet werden ist.  *Genauigkeit* muss es sich um einen numerischen Ausdruck sein. Wenn *Genauigkeit* eine positive Zahl ist, wird die Anzahl der angegebenen Länge decimal Positionen *Zahl* gerundet. Wenn *Genauigkeit* eine negative Zahl ist, wird auf der linken Seite neben dem Dezimalkomma gemäß Länge *Zahl* gerundet.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Der Typ der auszuführenden Vorgang. Wenn nicht angegeben oder auf 0 festlegen, wird die *Zahl* gerundet. Wenn ein anderer Wert als 0 angegeben wird, wird die *Zahl* gekürzt. Der Standardwert ist 0.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Round** gibt immer einen Wert. Ist Length negativ und größer als die Anzahl der Stellen vor dem Dezimalkomma, **Round** gibt 0 zurück. 
  

