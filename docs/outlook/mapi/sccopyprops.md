---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795437"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Betrifft**: Outlook 
  
Kopiert die Eigenschaften, die durch ein Array von [SPropValue](spropvalue.md) Strukturen zu einem neuen Ziel definiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> [in] Anzahl der Eigenschaften kopiert werden soll. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die definieren die Eigenschaften kopiert werden soll. Der Parameter _Rgprop_ muss nicht an den Anfang des Arrays zeigen, aber es muss zeigen Sie auf den Anfang einer der **SPropValue** Strukturen im Array. 
    
 _pvDst_
  
> [in] Zeiger auf die Ausgangsposition im Arbeitsspeicher, dem diese Funktion die Eigenschaften kopiert. 
    
 _PCB_
  
> [out] Optional Zeiger auf die Größe in Bytes, den Block mit Speicher durch den Parameter _PvDst_ . 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Eigenschaften wurden erfolgreich kopiert.
    
MAPI_E_INVALID_PARAMETER
  
> Unbekannte Eigenschaft vom Typ aufgetreten.
    
## <a name="remarks"></a>Bemerkungen

Das neue Array und ihre Daten befinden sich in einem Puffer mit einer einzelnen Reservierung erstellt, und die [ScRelocProps](screlocprops.md) -Funktion kann zum Anpassen der Zeiger in den einzelnen [SPropValue](spropvalue.md) Strukturen verwendet werden. Bevor Sie diese Anpassung sind der Zeiger gültig. 
  
 **ScCopyProps** behält die Reihenfolge der ursprünglichen Eigenschaft für Array der kopierten-Eigenschaft. 
  
Der Parameter _pcb_ ist optional. Wenn nicht NULL ist, wird es auf die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[ScDupPropset](scduppropset.md)

