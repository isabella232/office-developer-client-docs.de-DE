---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 279f8cf93a42cc886dbabbec7fbe94ac59e31593
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600976"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Informationen zur Unterstützung für die Freigabe eines Ordners bereit.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Ruft Informationen zur Unterstützung eines Ordners für die Freigabe ab.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Im Allgemeinen erfordert Microsoft Office Outlook einen MAPI-Speicheranbieter, um diese Schnittstelle zu implementieren, wenn der Anbieter einen Ordner freigeben möchte. Die Ausnahme ist der Exchange Server Speicheranbieter, der Ordner freigeben kann, ohne diese Schnittstelle zu implementieren.
  
Ein Client kann eine **[IMAPIFolder](imapifolderimapicontainer.md)** für **IFolderSupport** abfragen. Wenn dies erfolgreich ist, rufen **Sie IFolderSupport::GetSupportMask** auf, und überprüfen Sie, ob das **FS_SUPPORTS_SHARING-Bit** festgelegt werden soll. 
  

