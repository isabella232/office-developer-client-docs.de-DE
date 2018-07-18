---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Stellt die Eintrags-ID der standardmäßiger übermittlungsspeicher für das Konto an.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791179"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Stellt die Eintrags-ID der standardmäßiger übermittlungsspeicher für das Konto an.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x0018  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x00180102  <br/> |
|Access:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Abrufen Sie oder festlegen Sie dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp](iolkaccount-setprop.md), jeweils.
  
Einer der Nebeneffekte einen Speicher festlegen, wie die standardmäßiger übermittlungsspeicher für ein Konto besteht darin, dass beim Start von Outlook Outlook Suchordner für diesen Speicher, erstellt sofern diese noch nicht vorhanden, und den Informationsspeicher, in der Aufgabenleiste auflisten.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)

