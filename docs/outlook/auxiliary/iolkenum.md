---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791126"
---
# <a name="iolkenum"></a>IOlkEnum

Aufzählen von Konten als [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) -Objekte unterstützt. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
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

