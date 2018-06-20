---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Stellt eine ACCT_BIN-Struktur, die UID des ein Exchange-Konto enthält.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791211"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Stellt eine [ACCT_BIN](acct_bin.md) -Struktur, die UID des ein Exchange-Konto enthält. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x2009  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x20090102  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Verwenden Sie [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) , um sicherzustellen, wenn das Konto ein Exchange-Konto ist. Wenn dies der Fall, **Eigenschaft\_MAPI_EMSMDB_UID** ist eine **ACCT_BIN** , die die **EmsmdbUID**enthält, die die eindeutige ID, für die Exchange-Konto ist. Wenn das Konto nicht um ein Exchange-Konto handelt, ist diese Eigenschaft nicht definiert.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [Verwenden mehrerer Exchange-Konten](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Kanonische PidTagExchangeProfileSectionId-Eigenschaft](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

