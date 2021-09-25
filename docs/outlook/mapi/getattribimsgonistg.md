---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32988bc25e32ec3350a6e58e6418130a31f2095b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580188"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft attribute of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Nachrichtenspeicheranbieter  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameter

 _lpObject_
  
> [in] Zeiger auf ein **IMessage-Objekt,** das aus der [OpenIMsgOnIStg-Funktion](openimsgonistg.md) abgerufen wurde. 
    
 _lpPropTagArray_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, für die Attribute abgerufen werden sollen. 
    
 _lppPropAttrArray_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [SPropAttrArray-Struktur,](spropattrarray.md) die die abgerufenen Eigenschaftsattribute enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und wurde mit einem Eigenschaftentyp von PT_ERROR zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren. Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.** Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit **GetAttribIMsgOnIStg** abgerufen werden. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage-Objekte.** Sie sind nur gültig für **IMessage**-on- **IStorage-Objekte,** die von **OpenIMsgOnIStg** zurückgegeben werden. 
  
Die Anzahl und Positionen der Attribute im _Parameter "lppPropAttrArray"_ entsprechen der Anzahl und position der Eigenschaftstags im _LpPropTagArray-Parameter._ 
  

