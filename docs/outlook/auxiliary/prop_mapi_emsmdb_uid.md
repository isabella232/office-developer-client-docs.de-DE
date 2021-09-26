---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Stellt eine ACCT_BIN Struktur dar, die die UID eines Exchange Kontos enthält.
ms.openlocfilehash: 37718121de2aa8937dd9f1b78244d8da6fc0b662
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631139"
---
# <a name="prop_mapi_emsmdb_uid"></a>PROP_MAPI_EMSMDB_UID

Stellt eine [ACCT_BIN](acct_bin.md) Struktur dar, die die UID eines Exchange Kontos enthält. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2009  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20090102  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab.
  
Verwenden Sie [PROP_ACCT_IS_EXCH,](prop_acct_is_exch.md) um zu überprüfen, ob es sich bei dem Konto um ein Exchange Konto handelt. Wenn dies der Fall ist, ist **PROP \_ MAPI_EMSMDB_UID** eine **ACCT_BIN,** die die **emsmdbUID**(die eindeutige ID) für das Exchange-Konto enthält. Wenn es sich bei dem Konto nicht um ein Exchange Konto handelt, ist diese Eigenschaft nicht definiert.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [Verwenden mehrerer Exchange Konten](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Kanonische PidTagExchangeProfileSectionId-Eigenschaft](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

