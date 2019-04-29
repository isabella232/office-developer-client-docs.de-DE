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
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415775"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zur Unterstützung eines Ordners für die Freigabe.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[Getsupportmask aufrufen](ifoldersupport-getsupportmask.md)** <br/> |Ruft Informationen über die Unterstützung eines Ordners für die Freigabe ab.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Im Allgemeinen erfordert Microsoft Office Outlook einen MAPI-Speicheranbieter zum Implementieren dieser Schnittstelle, wenn der Anbieter einen Ordner freigeben möchte. Die Ausnahme ist der Exchange Server-Speicheranbieter, der Ordner freigeben kann, ohne diese Schnittstelle zu implementieren.
  
Ein Client kann eine **[IMAPIFolder](imapifolderimapicontainer.md)** für **IFolderSupport**Abfragen. Wenn dies erfolgreich ist, rufen Sie **IFolderSupport:: getsupportmask aufrufen** auf, und überprüfen Sie, ob das **FS_SUPPORTS_SHARING** -Bit festgelegt werden soll. 
  

