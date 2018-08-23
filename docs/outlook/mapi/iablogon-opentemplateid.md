---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a120fb1710bf2bd351d956e4d05eb0af346ef4c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583386"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Empfänger-Eintrag, der Daten in einer Host-Adressbuchanbieter hat.
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parameter

 _cbTemplateID_
  
> [in] Die Byteanzahl von in der Vorlagenbezeichner auf den durch den Parameter _LpTemplateID_ verwiesen. 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf die Vorlagenbezeichner oder **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfängers Eintrags geöffnet werden soll.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske der Flags verwendet, um anzugeben, wie den Eintrag dargestellt durch die ID der Vorlage zu öffnen. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Hostanbieter wird einen neuen Eintrag im Container basierend auf den Eintrag, dargestellt durch die ID der Vorlage erstellen. Die **OpenTemplateID** -Methode sollte entweder bestimmte Initialisierung des Eintrags für die Hostanbieter ausführen, mithilfe der [IMAPIProp: IUnknown](imapipropiunknown.md) Implementierung im Parameter _LpMAPIPropData_ oder Rückgabe eines benutzerdefinierten **IMAPIProp **-Schnittstelle im _LppMAPIPropNew_ -Parameter. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf die Hostanbieter Property-Objekt und Implementierung einer Schnittstelle abgeleitet **IMAPIProp**.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die den Typ des Zeigertools der Schnittstelle in der _LppMAPIPropNew_ -Parameter zurückgegeben werden soll. Übergeben von **null** gibt die messaging-Benutzeroberfläche, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf das gebundenen Property-Objekt und eine Implementierung einer Schnittstelle **IMAPIProp**abgeleitet.
    
 _lpMAPIPropSibling_
  
> [out] Reserviert. **null**muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der entsprechende Code wurde erfolgreich zu verwandten Daten in Hostanbieter gebunden.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine Vorlagen-IDs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Vorlage-ID in der _LpTemplateID_ -Parameter übergeben wird von der Adressbuchanbieter nicht erkannt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **OpenTemplateID** -Methode ist nur von adressbuchanbietern implementierte implementiert, die Kontrolle über Kopien der darin enthaltenen Einträge beibehalten werden, die in der Hostanbieter den Containern befinden. Anbieter, **die OpenTemplateID** implementieren, werden als fremden adressbuchanbietern implementierte bezeichnet. Hostanbieter [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) um kopierten Eintrag erstellen oder öffnen Sie den kopierten Eintrag aufrufen und MAPI für den Aufruf von **OpenTemplateID**übergibt. **OpenTemplateID** öffnet den Eintrag und bindet den Code, der mit Daten in Hostanbieter gesteuert. 
  
Statt eine Eintrags-ID verwenden, wird **OpenTemplateID** einer anderen-Eigenschaft, den Eintrag Vorlagenbezeichner, **PR_TEMPLATEID**verwendet. Vorlage Bezeichner sollte für Einträge unterstützt werden, dessen Code in ein Hostanbieter an Daten gebunden werden muss.
  
Einige Beispiele für beim Adressbuch-Dienstanbieter **OpenTemplateID** implementieren sollten sind wie folgt: 
  
- Die Daten in einem Eintrag der kopierten regelmäßig aktualisieren, damit es mit der ursprünglichen synchronisiert bleibt.
    
- Zum Implementieren der Funktionalität, mit denen Hostanbieter implementiert ist nicht möglich, wie dynamisches Auffüllen von Listen, die anhand von Daten auf einem Server in den Eintrag Detailtabelle angezeigt.
    
- Steuern die Interaktion zwischen Eigenschaften in der Hostanbieter-Eintrag und der ursprünglichen Eintrag, beispielsweise Netzwerke die **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Anzeige der Details, die verschiedene enthalten Komponenten der Adresse.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Hostanbieter kopiert oder von Ihrem Dienstanbieter ein Eintrag erstellt, und Sie die Implementierung einer Eigenschaft-Objekt über **OpenTemplateID geben**, behandeln Sie die meisten Anrufe verwalten den Eintrag. Da es bis zu Hostanbieter diese Anrufe an Sie weitergeleitet wird, kann Hostanbieter jedoch intercept jeder Aufruf und benutzerdefinierte Verarbeitung vor dem Weiterleiten des Anrufs führen.
  
Sie sollten die folgenden Richtlinien in Ihrer Eigenschaft Objekt Implementierungen verwenden:
  
- Wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird, bestimmen Sie, ob die Anforderung für eine berechnete Eigenschaft ist und es es zu behandeln ist. Übertragen Sie alle Anfragen für nicht berechneten Eigenschaften in Hostanbieter. 
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um zu öffnen eine Tabelle mit Ausnahme der Details Tabelle anzuzeigen, die Anforderung behandelt. Die meisten Tabellen werden nicht genau in Hostanbieter kopiert. Sie müssen die **IMAPITable** -Implementierung für diese angeforderten Tabellen generieren. Die Details Tabelle **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft muss für den Hostanbieter kopiert werden. Dies ermöglicht diesen Anbieter zum Generieren der Tabelle lokal. Möglicherweise möchten Sie die Display-Tabelle-Implementierung, um anzeigebenachrichtigungen Tabelle generieren umbrochen. 
    
- Wenn [IMAPIProp::SetProps](imapiprop-setprops.md) aufgerufen wird, kann die Daten von Hostanbieter überprüft werden, vor, sodass Sie die Eigenschaften festlegen. Sie können überprüfen, ob alle erforderlichen Eigenschaften festzulegen oder berechnet wurden. Den entsprechende Fehlermeldung-Wert zurück, wenn ein Fehler erkannt wurde, und, sofern möglich, eine beliebige zusätzliche Erläuterung über [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Wenn [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird, sollten die Hostanbieter Verarbeitung auszuführen, bevor Sie den Eintrag zu speichern. Speichern Sie alle Daten, die durch die geänderten Eigenschaften, wie eine neue Adresse ein, in der Hostanbieter Eintrag betroffen ist. 
    
Im Allgemeinen nehmen Sie die Implementierung des Eintrags, der Sie übergeben wieder Hostanbieter intercept alle Methoden zum Ausführen der kontextbezogenen Bearbeitung der relevanten Eigenschaften. Wenn das Flag FILL_ENTRY im _UlTemplateFlags_ -Parameter übergeben wird, legen Sie alle Eigenschaften für den Eintrag. 
  
Wenn Sie ein neues Property-Objekt in der _LppMAPIPropNew_ -Parameter zurückgeben möchten, rufen Sie die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) -Methode der Hostanbieter Property-Objekts einen Verweis zu verwalten. Nachdem sie von der gebundenen Objekt behandelt werden, müssen alle Anrufe über das gebundenen-Objekt, das die Implementierung **IMAPIProp** in _LppMAPIPropNew_ zurückgegeben, die entsprechende Methode in der Host Property-Objekt weitergeleitet werden. 
  
Die Eigenschaftenbezeichner der keine benannten Eigenschaften auf, die über Ihre gebundenen Property-Objekt übergeben werden befinden sich im Ihres Anbieters Bezeichner Namespace. Die Implementierung der [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode sollte die Namen der Eigenschaften festlegen, so, dass es Vorlage-spezifischen Aufgaben ausführen kann. Eigenschaften, die vom Dienstanbieter für dem Hostanbieter übergibt müssen auf ähnliche Weise auch in Ihren Namespace sein. Beispielsweise wenn Sie eine benannte Eigenschaft in **OpenTemplateID**festlegen, verwenden Sie Ihre-Bezeichner für den Namen – es, falls erforderlich, durch Aufrufen der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode erstellen. 
  
Wenn Sie die Eintrags-ID _LpTemplateID_übergebenen nicht kennen, geben Sie MAPI_E_UNKNOWN_ENTRYID zurück.
  
Weitere Informationen zum Arbeiten mit-Adressbuch Vorlage Adress-IDs finden Sie unter [als einen fremden Adressbuchanbieter fungiert](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

