---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389736"
---
# <a name="iolkenum"></a>IOlkEnum

Aufzählen von Konten als [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Objekte unterstützt. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Bereitgestellt von:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Ruft die Anzahl von Konten in den Enumerator ab.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Setzt den Enumerator auf den Anfang zurück.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Ruft das nächste Konto in den Enumerator ab.  <br/> |
|[Überspringen](iolkenum-skip.md) <br/> |Überspringt eine angegebene Anzahl von Konten in den Enumerator.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird von **IOlkAccountManager::EnumerateAccounts** zurückgegeben, wenn einen Enumerator von Konten zu erhalten. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

