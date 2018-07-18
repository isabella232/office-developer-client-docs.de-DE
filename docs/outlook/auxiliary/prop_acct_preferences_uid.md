---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Ruft den eindeutigen Bezeichner (UID) für den Benutzerprofildienst-Abschnitt, in dem die Vorgaben Konto gespeichert.
ms.openlocfilehash: 70e61264e5525f26e9f52e402bc785b544a0b90e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791195"
---
# <a name="propacctpreferencesuid"></a>PROP_ACCT_PREFERENCES_UID

Ruft den eindeutigen Bezeichner (UID) für den Benutzerprofildienst-Abschnitt, in dem die Vorgaben Konto gespeichert. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0 x 0022  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x00220102  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit der **PROP_ACCT_PREFERENCES_UID** Aufrufe [IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) Profilabschnitt abgerufen, der Konto Voreinstellungen enthält. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)

