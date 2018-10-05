---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Ruft den eindeutigen Bezeichner (UID) für den Benutzerprofildienst-Abschnitt, in dem die Vorgaben Konto gespeichert.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395293"
---
# <a name="propacctpreferencesuid"></a>PROP_ACCT_PREFERENCES_UID

Ruft den eindeutigen Bezeichner (UID) für den Benutzerprofildienst-Abschnitt, in dem die Vorgaben Konto gespeichert. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0 x 0022  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x00220102  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Mit der **PROP_ACCT_PREFERENCES_UID** Aufrufe [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) Profilabschnitt abgerufen, der Konto Voreinstellungen enthält. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)

