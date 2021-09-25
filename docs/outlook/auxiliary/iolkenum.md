---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: e18d23847744425bd7feb62dd615a4dcfa1c9287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625644"
---
# <a name="iolkenum"></a>IOlkEnum

Unterstützt das Aufzählen von Konten als [IUnknown-Objekte.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Bereitgestellt von:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getcount](iolkenum-getcount.md) <br/> |Ruft die Anzahl der Konten im Enumerator ab.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Setzt den Enumerator auf den Anfang zurück.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Ruft das nächste Konto im Enumerator ab.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Überspringt eine angegebene Anzahl von Konten im Enumerator.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird von **IOlkAccountManager::EnumerateAccounts** zurückgegeben, wenn ein Enumerator von Konten abgerufen wird. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

