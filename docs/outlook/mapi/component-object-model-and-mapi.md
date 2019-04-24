---
title: COM (Component Object Model) und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334468"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) und MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Windows SDK-Dokumentation enthält eine umfassende Erläuterung der Regeln für die Implementierung von Objekten, die dem Component Object Model (COM) entsprechen. Diese Regeln behandeln die folgenden Schritte:
  
- Entwerfen von Schnittstellen und Objekten.
    
- Implementieren Sie die [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle. 
    
- Speicher verwalten.
    
- Referenz Zählungen behandeln.
    
- Implementieren von Apartment-threaded-Objekten.
    
Obwohl alle MAPI-Objekte als COM-basiert gelten, da Sie Schnittstellen implementieren, die von [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)erben, weicht MAPI in einigen Situationen von den standardmäßigen com-Regeln ab. Diese Abweichung ermöglicht Entwicklern mehr Flexibilität in ihren Implementierungen. Beispielsweise beschreibt eine MAPI-Schnittstelle, wie jede beliebige COM-Schnittstelle, einen Vertrag zwischen Implementierer und Aufrufer. Sobald die Schnittstelle erstellt und veröffentlicht wurde, kann und wird Ihre Definition nicht geändert. MAPI weicht von dieser Beschreibung nicht ab, aber es entspannt die Beschreibung etwas. Implementierer können bestimmte Methoden nicht implementieren und einen der folgenden Fehlerwerte an den Aufrufer zurückgeben: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Die anderen Abweichungen von den standardmäßigen COM-Regeln werden in der folgenden Tabelle beschrieben.
  
|**COM-Programmier Regel**|**MAPI-Variation**|
|:-----|:-----|
|Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.  <br/> |MAPI-Schnittstellen sind so definiert, dass Unicode-oder ANSI-Zeichenfolgenparameter zulässig sind. Viele Methoden mit einem String-Parameter haben auch einen **ulFlags** -Parameter; die Breite eines String-Parameters wird durch den Wert des MAPI_UNICODE-Flags in **ulFlags**angegeben. Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag festgelegt ist.  <br/> |
|Alle Schnittstellenmethoden sollten einen Rückgabetyp von HRESULT aufweisen.  <br/> |MAPI verfügt über mindestens eine Methode, die einen nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Aufrufer und Implementierer sollten Speicher für Schnittstellenparameter mithilfe der standardmäßigen COM-Aufgabenzuweisungen zuweisen und freigeben.  <br/> |Alle MAPI-Methoden verwenden die verknüpften Zuordnungen [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [mapifreebufferfreigegeben](mapifreebuffer.md) , um Speicher für Schnittstellenparameter zu verwalten. Alle MAPI-Implementierungen von Schnittstellen, die von OLE definiert werden, wie [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), verwenden die standardMÄßIGen com-Aufgabenzuweisungen.  <br/> |
|Alle out-Zeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.  <br/> |MAPI-Schnittstellen erfordern, dass out-Zeigerparameter entweder auf NULL festgelegt oder unverändert bleiben, wenn eine Methode fehlschlägt. Alle MAPI-Implementierungen von Schnittstellen, die von OLE definiert wurden, haben bei einem Fehlschlagen explizit Parameter auf NULL festgelegt.  <br/> |
|Implementieren Sie nach Möglichkeit Aggregations Objekte.  <br/> |MAPI-Schnittstellen sind nicht aggregierbar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

