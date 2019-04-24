---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322099"
---
# <a name="iolkenum"></a>IOlkEnum

Unterstützt das Aufzählen von Konten als [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Objekte. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Bereitgestellt von:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Ruft die Anzahl der Konten im Enumerator ab.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Setzt den Enumerator auf den Anfang zurück.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Ruft das nächste Konto im Enumerator ab.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Überspringt eine angegebene Anzahl von Konten im Enumerator.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird von **IOlkAccountManager:: EnumerateAccounts** zurückgegeben, wenn ein Enumerator von Konten abgerufen wird. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

