---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Gibt die primäre Accountsendstamp für eine Nachricht an.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791177"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Gibt die primäre Konto "Senden" Zeitstempel für eine Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Bezeichner:  <br/> |0x0E28  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Konto  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt für ein MAPI-Message-Objekt. Bei einer empfangenen Nachricht gibt der primäre Konto Stempel "Senden" welches Konto eine Forward- oder eine Antwort mit gesendet werden sollen. Für eine ausgehende Nachricht an bestimmt, welches Konto zum Senden der Nachricht mit. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos ein, mit denen die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Kanonische PidTagPrimarySendAccount-Eigenschaft](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

