Three sections: Chicken, Beef, Sushi

Responsive layout:

Desktop: 3 sections in a row (each ~30% width)

Tablet: 2 sections in one row, Sushi on a new row

Mobile: All sections stack vertically

 some changes if required
 1. Add Clearfix to Prevent Container Collapse

Since we are  using float: left, the .container may collapse without clearfix.

we can this to file CSS:

.container::after {
  content: "";
  display: table;
  clear: both;
}


2. Improve Responsiveness with Padding/Spacing

To avoid cramped content on smaller screens, you can tweak spacing:

.menu-section p {
  margin-bottom: 10px;
  line-height: 1.5;
}

3. Smooth Font Scaling Across Devices

Adjust the heading size slightly more responsively:

.page-title {
  text-align: center;
  font-size: 2.5em;
  margin: 20px 0;
}
@media (max-width: 767px) {
  .page-title {
    font-size: 1.75em;
  }
}
