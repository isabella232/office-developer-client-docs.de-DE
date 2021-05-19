---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418897"
---
# <a name="prop_acct_delivery_store"></a>PROP_ACCT_DELIVERY_STORE

Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0018  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00180102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) bzw. [IOlkAccount::SetProp](iolkaccount-setprop.md)erhalten oder festlegen.
  
Einer der Nebeneffekte beim Festlegen eines Speichers als Standardzustellungsspeicher für ein Konto ist, dass Outlook beim Starten von Outlook Suchordner für diesen Speicher erstellt, falls diese noch nicht vorhanden sind, und den Speicher in der To-Do-Leiste auflisten.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)

