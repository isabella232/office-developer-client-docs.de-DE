---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Gibt den sekundären accountsendstamp für die Nachricht an.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327713"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Gibt das sekundäre Konto "Send"-Stempel für die Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Kennung:  <br/> |0x0E29  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt. Bei einer empfangenen Nachricht gibt der "Send"-Stempel des sekundären Kontos an, mit welchem Konto ein Forward oder eine Antwort gesendet werden soll, wenn die Weiterleitung oder Antwort nicht mit dem primären Konto gesendet werden kann. Bei einer ausgehenden Nachricht bestimmt das sekundäre Konto "Senden", mit welchem Konto die Nachricht gesendet werden soll, wenn die Nachricht nicht mit dem primären Konto versendet werden kann. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos, mit dem die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Kanonische Pidtagnextsendacct (-Eigenschaft](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

