---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792089"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport: IUnknown

  
  
**Betrifft**: Outlook 
  
Enthält Informationen zur Unterstützung für einen Ordner für die Freigabe.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Nachricht Speicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.  <br/> |
   
## <a name="remarks"></a>Hinweise

Im Allgemeinen erfordert Microsoft Office Outlook MAPI-Speicheranbieter diese Schnittstelle implementieren, wenn der Anbieter einen Ordner freigeben möchte. Die Ausnahme ist der Exchange-Server-Speicher-Anbieter, der Ordner freigeben kann, ohne dass diese Schnittstelle implementiert.
  
Ein Client kann ein **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**Abfragen. Wenn dies erfolgreich ist, rufen Sie **IFolderSupport::GetSupportMask** , und prüfen Sie, ob das Bit **FS_SUPPORTS_SHARING** festgelegt werden soll. 
  

