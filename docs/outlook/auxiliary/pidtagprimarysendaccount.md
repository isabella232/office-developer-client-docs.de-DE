---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Gibt den primären Accountsendstamp für eine Nachricht an.
ms.openlocfilehash: b4d0188d75cdf03a78c198377c03a885fce3654b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601233"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Gibt den primären "Senden"-Stempel des Kontos für eine Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Kennung:  <br/> |0x0E28  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Konto  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt. Bei einer empfangenen Nachricht gibt der primäre "Senden"-Stempel des Kontos an, mit welchem Konto eine Weiterleitung oder Antwort gesendet werden soll. Für eine ausgehende Nachricht wird bestimmt, mit welchem Konto die Nachricht gesendet werden soll. Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) Wert aus der [IOlkAccount-Schnittstelle](iolkaccount.md) des Kontos, mit dem die Nachricht gesendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)
- [MAPI-Eigenschaften](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [PidTagPrimarySendAccount (kanonische Eigenschaft)](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

