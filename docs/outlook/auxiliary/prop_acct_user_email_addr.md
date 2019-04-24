---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Gibt die e-Mail-Adresse für das Konto an.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326530"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Gibt die e-Mail-Adresse für das Konto an.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x000C  <br/> |
|Eigenschafts:  <br/> |PT_UNICODE  <br/> |
|Property-Tag:  <br/> |0x000C001F  <br/> |
|Access  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **PROP_ACCT_USER_EMAIL_ADDR** wird nicht in jedem Konto vorhanden sein. Ein Exchange-Konto kann beispielsweise [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , aber nicht **PROP_ACCT_USER_EMAIL_ADDR**haben, während bei einem SMTP/POP3-Konto die Situation umgekehrt wird.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

