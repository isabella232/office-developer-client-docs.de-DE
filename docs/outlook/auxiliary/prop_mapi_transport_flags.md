---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt transporteinstellungen, die Outlook verwendet, um die erforderlichen Aufgaben zu ermitteln und die Elemente der Benutzeroberfläche (UI) zu deaktivieren, die das Konto nicht unterstützt.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791192"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Stellt transporteinstellungen, die Outlook verwendet, um die erforderlichen Aufgaben zu ermitteln und die Elemente der Benutzeroberfläche (UI) zu deaktivieren, die das Konto nicht unterstützt.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x2010  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x20100102  <br/> |
|Access:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Abrufen Sie oder festlegen Sie dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp](iolkaccount-setprop.md), jeweils.
  
Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden kann, jedoch keine Nachrichten empfangen. In diesem Fall wird Outlook Benutzeroberfläche, die auf diese Art von Konten (beispielsweise die Benutzeroberfläche für **Senden/Empfangen**) nicht anwendbar ist deaktiviert.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

