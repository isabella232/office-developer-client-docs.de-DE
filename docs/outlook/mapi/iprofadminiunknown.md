---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577415"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwaltung von Benutzerprofilen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verfügbar gemacht von:  <br/> |Profile Administration-Objekt  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProfAdmin  <br/> |
|Zeigertyp:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die auf ein Profil Administration-Objekt aufgetreten sind.  <br/> |
|["GetProfileTable"](iprofadmin-getprofiletable.md) <br/> |Bietet Zugriff auf die Benutzerprofildienst-Tabelle eine Tabelle mit Informationen zu allen verfügbaren Profilen.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Erstellt ein neues Profil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Löscht ein Profil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Veraltet. Ändert das Kennwort für ein Profil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Kopiert ein Profil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Weist einen neuen Namen zu einem Profil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Aktiviert oder deaktiviert eine Client-Standardprofil.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Bietet Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Nachrichtendienste in einem Profil.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

