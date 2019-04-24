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
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334748"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Empfängereintrag mit Daten, die sich in einem Host-Adressbuchanbieter befinden.
  
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
  
> in Die Anzahl der Bytes im Vorlagenbezeichner, auf die durch den _lpTemplateID_ -Parameter verwiesen wird. 
    
 _lpTemplateID_
  
> in Ein Zeiger auf den Vorlagenbezeichner oder die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfänger Eintrags, der geöffnet werden soll.
    
 _ulTemplateFlags_
  
> in Eine Bitmaske von Flags, mit der angegeben wird, wie der durch den Vorlagenbezeichner dargestellte Eintrag geöffnet wird. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Der Hostanbieter erstellt anhand des vom Vorlagenbezeichner dargestellten Eintrags einen neuen Eintrag im Container. Die **IABLogon::** opentemplatecollection-Methode sollte entweder eine bestimmte Initialisierung des Eintrags des Host Anbieters durchführen, indem Sie die [IMAPIProp: IUnknown](imapipropiunknown.md) -Implementierung im _lpMAPIPropData_ -Parameter verwenden oder eine benutzerdefinierte IMAPIProp zurückgeben. ** **Schnittstellenimplementierung im _lppMAPIPropNew_ -Parameter. 
    
 _lpMAPIPropData_
  
> in Ein Zeiger auf das Property-Objekt des Host Anbieters und die Implementierung einer von **IMAPIProp**abgeleiteten Schnittstelle.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die den Typ des Schnittstellenzeigers darstellt, der im _lppMAPIPropNew_ -Parameter zurückgegeben werden soll. Durch das Übergeben von **null** wird die standardmäßige Messaging-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md)zurückgegeben.
    
 _lppMAPIPropNew_
  
> Out Ein Zeiger auf das gebundene Property-Objekt und eine Implementierung einer von **IMAPIProp**abgeleiteten Schnittstelle.
    
 _lpMAPIPropSibling_
  
> Out Reserviert muss **null**sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der entsprechende Code wurde erfolgreich an verknüpfte Daten im Hostanbieter gebunden.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine Vorlagen-IDs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im _lpTemplateID_ -Parameter übergebene Vorlagenbezeichner wird vom Adressbuchanbieter nicht erkannt. 
    
## <a name="remarks"></a>Bemerkungen

Die **IABLogon::** opentemplatecode-Methode wird nur von Adressbuch Anbietern implementiert, die die Kontrolle über Kopien Ihrer Einträge behalten müssen, die sich in den Containern von Hostanbietern befinden. Anbieter, die **** opentemplatecode implementieren, werden als fremde Adressbuchanbieter bezeichnet. Host Anbieter rufen [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode auf, um einen kopierten Eintrag zu erstellen oder den kopierten Eintrag zu öffnen, und MAPI übergibt den Aufruf an **IABLogon::** opentemplatecode. **IABLogon::** opentemplatecode öffnet den Eintrag und bindet den Code, der ihn steuert, an Daten im Hostanbieter. 
  
Statt eine Eintrags-ID zu verwenden, verwendet **IABLogon::** opentemplatecode eine andere Eigenschaft, den Vorlagenbezeichner des Eintrags, **PR_TEMPLATEID**. Vorlagenbezeichner sollten für Einträge unterstützt werden, deren Code an Daten in einem Hostanbieter gebunden werden muss.
  
Einige Beispiele dafür, wann ein Adressbuchanbieter **IABLogon::** opentemplateserver implementieren sollte, lauten wie folgt: 
  
- So aktualisieren Sie die Daten für einen kopierten Eintrag in regelmäßigen Abständen, damit Sie mit dem Original synchronisiert bleiben.
    
- Zum Implementieren von Funktionen, die der Hostanbieter nicht implementieren kann, wie das dynamische Auffüllen einer Liste, die in der Details-Tabelle des Eintrags angezeigt wird, aus Daten auf einem Server.
    
- Um die Interaktion zwischen den Eigenschaften im Eintrag des Host Anbieters und dem ursprünglichen Eintrag zu steuern, wie etwa dem Berechnen des **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Detailanzeige, die unterschiedliche Komponenten der Adresse.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Hostanbieter einen Eintrag von Ihrem Anbieter kopiert oder erstellt und Sie eine Property-Objekt Implementierung über **IABLogon::** opentemplatecollection bereitstellen, behandeln Sie die meisten Aufrufe, um den Eintrag zu verwalten. Da der Hostanbieter diese Anrufe an Sie weiterleiten muss, kann der Hostanbieter jedoch alle Anrufe abfangen und eine benutzerdefinierte Verarbeitung durchführen, bevor der Anruf weitergeleitet wird.
  
Sie sollten die folgenden Richtlinien in ihren Property-Objekt-Implementierungen verwenden:
  
- Wenn [IMAPIProp::](imapiprop-getprops.md) GetProps aufgerufen wird, bestimmen Sie, ob es sich bei der Anforderung um eine berechnete Eigenschaft handelt, und behandeln Sie diese. Übertragen Sie alle Anforderungen für nicht berechnete Eigenschaften an den Hostanbieter. 
    
- Wenn [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um eine Tabelle mit Ausnahme der Details-Anzeigetabelle zu öffnen, behandeln Sie die Anforderung. Die meisten Tabellen können nicht genau in den Hostanbieter kopiert werden. Sie müssen die **IMAPITable** -Implementierung für diese angeforderten Tabellen generieren. Die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft der Details-Tabelle muss in den Hostanbieter kopiert werden. Dies ermöglicht es diesem Anbieter, die Tabelle lokal zu generieren. Möglicherweise möchten Sie die Implementierung der Display-Tabelle umbrechen, um Anzeige Tabellen Benachrichtigungen zu generieren. 
    
- Wenn [IMAPIProp::](imapiprop-setprops.md) SetProps aufgerufen wird, kann der Hostanbieter die Daten überprüfen, bevor Sie die Eigenschaften festlegen. Sie können überprüfen, ob alle erforderlichen Eigenschaften festgelegt oder berechnet wurden. Wenn ein Fehler erkannt wird, geben Sie den entsprechenden Fehlerwert und, falls möglich, weitere Erläuterungen über [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md)zurück.
    
- Wenn [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) aufgerufen wird, kann der Hostanbieter die Verarbeitung vor dem Speichern des Eintrags ausführen. Sie sollten alle Daten, die von den geänderten Eigenschaften betroffen sind, wie beispielsweise eine neue Adresse, im Eintrag des Host Anbieters speichern. 
    
Im Allgemeinen sollten Sie die Implementierung des Eintrags, den Sie an den Hostanbieter zurückgeben, abfangen, um alle Methoden zum Durchführen einer kontextspezifischen Manipulation der relevanten Eigenschaften zu übernehmen. Wenn das FILL_ENTRY-Flag im _ulTemplateFlags_ -Parameter übergeben wird, legen Sie alle Eigenschaften für den Eintrag fest. 
  
Wenn Sie ein neues Property-Objekt im _lppMAPIPropNew_ -Parameter zurückgeben, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Property-Objekts des Host Anbieters auf, um einen Verweis zu verwalten. Alle Aufrufe über das gebundene Objekt, die die **IMAPIProp** -Implementierung in _lppMAPIPropNew_ zurückgegeben wird, sollten an Ihre entsprechende Methode im Host Property-Objekt weitergeleitet werden, nachdem Sie vom gebundenen Objekt behandelt werden. 
  
Die Eigenschaftenbezeichner aller benannten Eigenschaften, die durch das gebundene Property-Objekt übergeben werden, befinden sich im Bezeichner-Namespace Ihres Anbieters. Durch die Implementierung der [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode sollten die Namen der Eigenschaften bestimmt werden, sodass Vorlagenspezifische Aufgaben ausgeführt werden können. Entsprechend müssen Eigenschaften, die Ihr Anbieter an den Hostanbieter übergibt, auch in Ihrem Namespace sein. Wenn Sie beispielsweise eine benannte Eigenschaft in openTemplatecode festlegen, sollten Sie einen ihrer Bezeichner für den Namen verwenden, um ihn gegebenenfalls zu erstellen, indem Sie die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode aufrufen. **** 
  
Wenn Sie den in _lpTemplateID_übergebenen Eintragsbezeichner nicht erkennen, geben Sie MAPI_E_UNKNOWN_ENTRYID zurück.
  
Weitere Informationen zum Arbeiten mit Adressbuchvorlagen-IDs finden Sie unter [agieren als ein fremder Adressbuchanbieter](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Kanonische Pidtagtemplateid (-Eigenschaft](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

