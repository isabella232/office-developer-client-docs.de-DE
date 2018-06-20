---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Gibt die e-Mail-Adresse für das Konto an.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791194"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Gibt die e-Mail-Adresse für das Konto an.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x000C  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschafts-Tag:  <br/> |0x000C001F  <br/> |
|Access:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Hinweise

 **PROP_ACCT_USER_EMAIL_ADDR** voraussichtlich nicht auf jedem Konto vorhanden sein. Beispielsweise konnte ein Exchange-Konto verfügen, [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) jedoch nicht **PROP_ACCT_USER_EMAIL_ADDR**, während für ein SMTP/POP3-Konto an, die über diese Situation rückgängig gemacht.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

