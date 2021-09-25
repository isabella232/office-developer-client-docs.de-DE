---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.
ms.openlocfilehash: aec2e379c97b8d1088b86c0d663c177b23f042cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601212"
---
# <a name="prop_acct_delivery_store"></a>PROP_ACCT_DELIVERY_STORE

Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0018  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00180102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dient zum Abrufen oder Festlegen dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp.](iolkaccount-setprop.md)
  
Einer der Nebeneffekte beim Festlegen eines Speichers als Standardzustellungsspeicher für ein Konto besteht darin, dass Outlook beim Starten von Outlook Suchordner für diesen Speicher erstellt, falls sie noch nicht vorhanden sind, und den Speicher in der To-Do Leiste auflisten.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)

