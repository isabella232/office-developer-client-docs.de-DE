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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564171"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zur Unterstützung für einen Ordner für die Freigabe.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Nachricht Speicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Im Allgemeinen erfordert Microsoft Office Outlook MAPI-Speicheranbieter diese Schnittstelle implementieren, wenn der Anbieter einen Ordner freigeben möchte. Die Ausnahme ist der Exchange-Server-Speicher-Anbieter, der Ordner freigeben kann, ohne dass diese Schnittstelle implementiert.
  
Ein Client kann ein **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**Abfragen. Wenn dies erfolgreich ist, rufen Sie **IFolderSupport::GetSupportMask** , und prüfen Sie, ob das Bit **FS_SUPPORTS_SHARING** festgelegt werden soll. 
  

