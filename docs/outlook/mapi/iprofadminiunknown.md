---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a6387de14e7b4ee513168ddd65383c39481c8699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620576"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwaltung von Profilen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Profilverwaltungsobjekt  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProfAdmin  <br/> |
|Zeigertyp:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](iprofadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für ein Profilverwaltungsobjekt aufgetreten ist.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Bietet Zugriff auf die Profiltabelle, eine Tabelle, die Informationen zu allen verfügbaren Profilen enthält.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Erstellt ein neues Profil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Löscht ein Profil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Veraltet. Ändert das Kennwort für ein Profil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Kopiert ein Profil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Weist einem Profil einen neuen Namen zu.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Legt das Standardprofil eines Clients fest oder löscht es.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Bietet Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt, um Änderungen an den Nachrichtendiensten in einem Profil vorzunehmen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

