---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Gibt die sekundäre Accountsendstamp für die Nachricht an.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396477"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Gibt die sekundäre Konto "Senden" für die Nachricht.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Kennung:  <br/> |0x0E29  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt für ein MAPI-Message-Objekt. Bei einer empfangenen Nachricht gibt der sekundären Konto-Stempel "Senden" welches Konto mit, eine Forward- oder eine Antwort gesendet werden soll, wenn mit das primäre Konto der weiterleiten oder der Antwort gesendet werden kann. Für eine ausgehende Nachricht bestimmt sekundäre Konto "Stempel senden" mit welchem Konto zum Senden der Nachricht, wenn die Nachricht mit das primäre Konto gesendet werden kann. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos ein, mit denen die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [PidTagNextSendAcct (kanonische Eigenschaft)](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

