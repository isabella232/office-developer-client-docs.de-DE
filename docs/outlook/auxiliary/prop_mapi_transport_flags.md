---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt Transporteinstellungen dar, die Outlook verwendet, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die Benutzeroberflächenelemente zu deaktivieren, die das Konto nicht unterstützt.
ms.openlocfilehash: 9137fb724fc7702a852861d8f59e5bce1141eb1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605316"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

Stellt Transporteinstellungen dar, die Outlook verwendet, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die Benutzeroberflächenelemente zu deaktivieren, die das Konto nicht unterstützt.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2010  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20100102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dient zum Abrufen oder Festlegen dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp.](iolkaccount-setprop.md)
  
Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden, aber keine Nachrichten empfangen kann. In diesem Fall deaktiviert Outlook die Benutzeroberfläche, die nicht für diese Art von Konten gilt (z. B. die Benutzeroberfläche für **Senden/Empfangen).**
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

