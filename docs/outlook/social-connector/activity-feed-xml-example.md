---
title: Beispiel für eine Aktivität Feed XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: Das XML-Beispiel in diesem Thema wird, dass ein Aktivitätsfeed an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die ISocialSession2::GetActivitiesEx-Methode für ein social Network ruft XML-Zeichenfolge.
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795947"
---
# <a name="activity-feed-xml-example"></a>Beispiel für eine Aktivität Feed XML

Das XML-Beispiel in diesem Thema wird ein Aktivitätsfeed an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode für ein social Network ruft XML-Zeichenfolge. 
  
Das Beispiel zeigt die **ActivityFeed** XML, das die folgenden vier Aktivitäten enthält, jeweils getrennt durch das Element **ActivityDetails** und matching eine Vorlage für die Zwecke anzuzeigen: 
  
- Ein Profilbild aktualisieren, indem Sie Melissa Macbeth, dessen **OwnerID** im sozialen Netzwerk 4667647 ist. Diese Aktivität gibt drei Vorlagenvariablen vom Typ **PublisherVariable**, **ListVariable**und **PictureVariable** (die in **ListVariable**eingeschlossen wird). Diese Variablen geben die Person, die die Aktivitätsfeed Element und Informationen für das Bild zu aktualisierenden (mithilfe der **Name**, **Value**, **AltText**und **Href** untergeordnete Elemente des **PictureVariable**) veröffentlicht.
    
- Ein Profilbild aktualisieren, indem Sie Michael Affronti, deren **OwnerID** im sozialen Netzwerk 5015012 ist. Ähnlich wie die letzte Aktivität, gibt diese Aktivität drei Vorlagenvariablen vom Typ **PublisherVariable**, **ListVariable**und **PictureVariable**. Diese Variablen geben die Person, die die Aktivitätsfeed Element und Informationen für das Bild zu aktualisierenden veröffentlicht.
    
- Von Michael Affronti, mit der gleichen **OwnerID** des 5015012 als die letzte Aktivität Statusinformationen. Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **PublisherVariable** und **TextVariable**an. **PublisherVariable** gibt die Person, die die Aktivitätsfeed Element veröffentlicht und **TextVariable** enthält den **Wert** der Statuszeile`is hiking on Mount Rainier this weekend!`
    
- Von Michael Affronti, mit der gleichen **OwnerID** des 5015012 als die letzten beiden Aktivitäten Blogbeitrag. Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **PublisherVariable** und **LinkVariable**an. **PublisherVariable** gibt die Person, die die Aktivität veröffentlicht feed Element und **LinkVariable** enthält weitere Informationen (angegeben durch den **Namen**, **Text**und **Value** untergeordnete Elemente des **LinkVariable**) Informationen zu den Blogbeitrag.
    
Jede der vier Aktivitäten gibt einen **TemplateID** -Wert, der eine der drei Vorlagen für die **Vorlagen** -Element angegebenen entspricht. Jede Vorlage ist in einem eigenen **ActivityTemplateContainer** -Element identifizierten ein **TemplateID** -Wert, der auch verwendet wird, um eine Aktivität anzuzeigen, die den gleichen Wert **TemplateID** verfügt. 
  
Eine ausführliche Beschreibung der XML-Elemente im Beispiel verwendet finden Sie unter den folgenden Themen: 
  
- [Übersicht über XML-Code für eine Aktivität Element-Feed](overview-of-xml-for-an-activity-feed-item.md)
    
- [ActivityDetails Element](activitydetails-element.md)
    
- [ActivityTemplateContainer Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die XML-Daten des vier Aktivitäten **ActivityFeed** : zwei Bild Updates, Statusinformationen und Blogbeiträgen profile. Der XML-Code gibt zudem drei Aktivität Anzeigevorlagen für den zugehörigen Aktivitäten anzeigen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a>Siehe auch

- [OSC-Anbieter XML-Beispielen](osc-provider-xml-examples.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md) 
- [Funktionen XML-Beispiel](capabilities-xml-example.md)  
- [Freunde XML-Beispiel](friends-xml-example.md)
- [Outlook Connector für soziale Netzwerke Anbieter XML-Schema](outlook-social-connector-provider-xml-schema.md)

