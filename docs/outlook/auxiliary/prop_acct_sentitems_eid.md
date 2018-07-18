---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto an.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791182"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto an. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0 x 0020  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x00200102  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
**Gesendete Elemente**ist der Standardordner für gesendete Elemente.
  
Diese Eigenschaft ist schreibgeschützt für POP3- und IMAP-Konten. Sie versuchen, diese Eigenschaft für diese Typen von Konten festzulegen, gibt **E_ACCT_NOT_FOUND**zurück. 
  

