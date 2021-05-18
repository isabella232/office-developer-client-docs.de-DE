---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Stellt eine ACCT_BIN, die die UID eines Exchange-Kontos enthält.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326551"
---
# <a name="prop_mapi_emsmdb_uid"></a>PROP_MAPI_EMSMDB_UID

Stellt eine [ACCT_BIN,](acct_bin.md) die die UID eines Exchange-Kontos enthält. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2009  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20090102  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)
  
Verwenden [PROP_ACCT_IS_EXCH,](prop_acct_is_exch.md) um zu überprüfen, ob es sich bei dem Konto um ein Exchange-Konto handelt. Wenn dies **\_ der** MAPI_EMSMDB_UID ist,  ist prop ACCT_BIN, das **die emsmdbUID** enthält, die die eindeutige ID für das Exchange-Konto ist. Wenn es sich bei dem Konto nicht um ein Exchange-Konto handelt, ist diese Eigenschaft nicht definiert.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [Verwenden mehrerer Exchange-Konten](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Kanonische PidTagExchangeProfileSectionId-Eigenschaft](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

