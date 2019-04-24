---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt Transporteinstellungen dar, die Outlook zum Ermitteln der erforderlichen Synchronisierungsaufgaben verwendet, und zum Deaktivieren der Benutzeroberflächenelemente, die das Konto nicht unterstützt.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326481"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Stellt Transporteinstellungen dar, die Outlook zum Ermitteln der erforderlichen Synchronisierungsaufgaben verwendet, und zum Deaktivieren der Benutzeroberflächenelemente, die das Konto nicht unterstützt.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2010  <br/> |
|Eigenschafts:  <br/> |PT_BINARY  <br/> |
|Property-Tag:  <br/> |0x20100102  <br/> |
|Access  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Abrufen oder Festlegen dieser Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md) oder [IOlkAccount:: setprop](iolkaccount-setprop.md), beziehungsweise.
  
Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden, aber keine Nachrichten empfangen kann. In diesem Fall deaktiviert Outlook die Benutzeroberfläche, die für diese Art von Konten nicht gilt (beispielsweise die Benutzeroberfläche für **senden/empfangen**).
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

