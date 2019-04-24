---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Gibt den primären accountsendstamp für eine Nachricht an.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327706"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Gibt das primäre Konto "Send"-Stempel für eine Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Kennung:  <br/> |0x0E28  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Konto  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt. Bei einer empfangenen Nachricht gibt der "Send"-Stempel des primären Kontos an, mit welchem Konto ein Forward oder eine Antwort gesendet werden soll. Bei einer ausgehenden Nachricht bestimmt Sie, mit welchem Konto die Nachricht gesendet wird. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos, mit dem die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Kanonische Pidtagprimarysendaccount (-Eigenschaft](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

