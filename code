 package get_country_from_IP_address_in_JAVA;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.URL;
public class Get_Location_From_IP {
  public Location_Use_workforwin get_ip_Details(String ip) {
      String key = "9d6jinufcfdfacc213c7ddf4ef911dfe97b55e4696be3732bf8302876c09ebad06b";
      ip = ip.trim();
      Location_Use_workforwin obj_Location_Use_workforwin = new Location_Use_workforwin();
      System.out.println("The ip adress is before " + ip + );
      try {
          if (ip.contains(",")) {
              String temp_ip[] = ip.split(",");
              ip = temp_ip[1].trim();
          }
      } catch (Exception e) {    // this is for handle exception
      }
      System.out.println("The ip adress is after " + ip + );
      URL url;
      try {
          url = new URL("https://api.ipinfodb.com/v3/ip-city/?key=" + enter your key + "&ip=" + ip);
          //use your own key and for update your key  <--  go to this link https://api.ipinfodb.com/v3/ip-city/?key
          BufferedReader br = new BufferedReader(new InputStreamReader(url.openStream()));
          String strTemp = "";
          String temporaray = "";
          String temp_array[] = null;
          while (null != (strTemp = br.readLine())) {
              temporaray = strTemp;
          }
          temp_array = temporaray.split(";");
          System.out.println("String length is " + temp_array.length);
          int length = temp_array.length;
          if (length == 11) {
              obj_Location_Use_workforwin.setIp_address(ip);
              if (temp_array[3] != null) {
                  obj_Location_Use_workforwin.setCountry_code(temp_array[3]);
              }
              if (temp_array[4] != null) {
                  obj_Location_Use_workforwin.setCountry(temp_array[4]);
              }
              if (temp_array[5] != null) {
                  obj_Location_Use_workforwin.setState(temp_array[5]);
              }
              if (temp_array[6] != null) {
                  obj_Location_Use_workforwin.setCity(temp_array[6]);
              }
              if (temp_array[7] != null) {
                  obj_Location_Use_workforwin.setZip(temp_array[7]);
              }
              if (temp_array[8] != null) {
                  obj_Location_Use_workforwin.setLat(temp_array[8]);
              }
              if (temp_array[9] != null) {
                  obj_Location_Use_workforwin.setLon(temp_array[9]);
              }
              if (temp_array[10] != null) {
                  obj_Location_Use_workforwin.setUtc_offset(temp_array[10]);
              }
          }
      } catch (Exception e) {
          e.printStackTrace();
      }
      return obj_Location_Use_workforwin;
  }
  public static void main(String[] args) {
      Get_Location_From_IP obj_Get_Location_From_IP = new Get_Location_From_IP();
      Location_Use_workforwin obj_Location_Use_workforwin = obj_Get_Location_From_IP.get_ip_Details("49.153.63.12");
      System.out.println("IP Address-" + obj_Location_Use_workforwin.getIp_address());
      System.out.println("Country Code- " + obj_Location_Use_workforwin.getIp_address());
      System.out.println("Country Name " + obj_Location_Use_workforwin.getCountry());
      System.out.println("State Name " + obj_Location_Use_workforwin.getState());
      System.out.println("City Name " + obj_Location_Use_workforwin.getCity());
      System.out.println("ZIP Code " + obj_Location_Use_workforwin.getZip());
      System.out.println("Latitude " + obj_Location_Use_workforwin.getLat());
      System.out.println("Longitude " + obj_Location_Use_workforwin.getLon());
      System.out.println("Offset/Time :" + obj_Location_Use_workforwin.getUtc_offset());
  }
}
