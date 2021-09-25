---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.
ms.openlocfilehash: e9073a5b113ddd1181cb46ce44ac238833893636
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614346"
---
# <a name="prop_acct_sentitems_eid"></a>PROP_ACCT_SENTITEMS_EID

Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0020  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00200102  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab.
  
Der Standardordner für gesendete Elemente ist **"Gesendete Elemente".**
  
Diese Eigenschaft ist für POP3- und IMAP-Konten schreibgeschützt. Wenn Sie versuchen, diese Eigenschaft für diese Arten von Konten festzulegen, **wird E_ACCT_NOT_FOUND** zurückgegeben. 
  

