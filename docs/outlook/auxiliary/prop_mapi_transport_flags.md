---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt Transporteinstellungen dar Outlook die verwendet werden, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die benutzeroberflächenelemente zu deaktivieren, die vom Konto nicht unterstützt werden.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404526"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

Stellt Transporteinstellungen dar Outlook die verwendet werden, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die benutzeroberflächenelemente zu deaktivieren, die vom Konto nicht unterstützt werden.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2010  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20100102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) bzw. [IOlkAccount::SetProp](iolkaccount-setprop.md)erhalten oder festlegen.
  
Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden, aber keine Nachrichten empfangen kann. In diesem Fall deaktiviert Outlook benutzeroberfläche, die nicht für diesen Typ von Konten gilt (z. B. die Benutzeroberfläche für **Senden/Empfangen**).
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

