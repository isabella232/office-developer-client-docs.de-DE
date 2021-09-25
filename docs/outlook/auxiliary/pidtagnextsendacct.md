---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Gibt den sekundären Accountsendstamp für die Nachricht an.
ms.openlocfilehash: 4acc8639be3b09a2a12fc402c7fc5bc2463af4db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557113"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Gibt den Stempel "senden" des sekundären Kontos für die Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Kennung:  <br/> |0x0E29  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt. Bei einer empfangenen Nachricht gibt der sekundäre "Senden"-Stempel des Kontos an, mit welchem Konto eine Weiterleitung oder Antwort gesendet werden soll, wenn die Weiterleitung oder Antwort nicht mit dem primären Konto gesendet werden kann. Bei ausgehenden Nachrichten bestimmt der Stempel "Senden" des sekundären Kontos, mit welchem Konto die Nachricht gesendet werden soll, ob die Nachricht nicht mit dem primären Konto gesendet werden kann. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) Wert aus der [IOlkAccount-Schnittstelle](iolkaccount.md) des Kontos, mit dem die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [PidTagNextSendAcct (kanonische Eigenschaft)](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

